---
title: 'CA2301: 먼저 BinaryFormatter.Binder를 설정하지 않고 BinaryFormatter.Deserialize를 호출하지 마세요.'
ms.date: 04/05/2019
ms.topic: reference
author: dotpaul
ms.author: paulming
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: d90ed71c1d5ca4cbfdcf8e500e1d176519a2fdff
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62541573"
---
# <a name="ca2301-do-not-call-binaryformatterdeserialize-without-first-setting-binaryformatterbinder"></a>CA2301: 먼저 BinaryFormatter.Binder를 설정하지 않고 BinaryFormatter.Deserialize를 호출하지 마세요.

|||
|-|-|
|TypeName|DoNotCallBinaryFormatterDeserializeWithoutFirstSettingBinaryFormatterBinder|
|CheckId|CA2301|
|범주|Microsoft.Security|
|변경 수준|주요 변경 아님|

## <a name="cause"></a>원인

A <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType> deserialization 메서드를 호출 하거나 하지 않고 참조 된 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> 속성 집합입니다.

## <a name="rule-description"></a>규칙 설명

[!INCLUDE[insecure-deserializers-description](includes/insecure-deserializers-description-md.md)]

이 규칙을 찾습니다 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType> 메서드 호출 또는 참조 deserialization 때 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> 없는 해당 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> 설정 합니다. 사용 하 여 모든 deserialization을 허용 하지 않도록 하려는 경우 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> 에 관계 없이 합니다 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> 속성을이 규칙을 사용 하지 않도록 설정 및 [CA2302](ca2302-ensure-binaryformatter-binder-is-set-before-calling-binaryformatter-deserialize.md), 규칙을 사용 하도록 설정 하 고 [CA2300](ca2300-do-not-use-insecure-deserializer-binaryformatter.md)합니다.

## <a name="how-to-fix-violations"></a>위반 문제를 해결하는 방법

- 가능한 경우 보안 직렬 변환기를 대신 사용 하 고 **공격자가 임의의 형식을 deserialize 하는 데 지정 하지**합니다. 안전한 일부 serializer는 다음과 같습니다.
  - <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType>
  - <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType>
  - <xref:System.Web.Script.Serialization.JavaScriptSerializer?displayProperty=nameWithType> -사용해 서는 안 <xref:System.Web.Script.Serialization.SimpleTypeResolver?displayProperty=nameWithType>합니다. 형식 확인자를 사용 해야 하는 경우 예상 되는 목록에 deserialize 된 형식을 제한 합니다.
  - <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType>
  - NewtonSoft Json.NET-TypeNameHandling.None를 사용 합니다. TypeNameHandling에 대 한 다른 값을 사용 해야 하는 경우 사용자 지정 ISerializationBinder 사용 하 여 예상된 목록에 deserialize 된 형식을 제한 합니다.
  - 프로토콜 버퍼
- Serialize 된 데이터 변조 증명을 확인 합니다. Serialization 한 후 serialize 된 데이터를 암호화 하 여 로그인 합니다. Deserialization을 수행 하기 전에 암호화 서명을 확인 합니다. 노출 되는 암호화 키를 보호 하 고 키 회전에 대 한 설계 합니다.
- Deserialize 된 형식을 제한 합니다. 사용자 지정 구현 <xref:System.Runtime.Serialization.SerializationBinder?displayProperty=nameWithType>합니다. 로 역직렬화 하기 전에 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter>로 설정 합니다 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> 사용자의 인스턴스에 대 한 속성 <xref:System.Runtime.Serialization.SerializationBinder>합니다. 재정의 된 <xref:System.Runtime.Serialization.SerializationBinder.BindToType%2A> 메서드, 형식에 예기치 않은 경우 다음 예외를 throw 합니다.

## <a name="when-to-suppress-warnings"></a>경고를 표시 하는 경우

[!INCLUDE[insecure-deserializers-common-safe-to-suppress](includes/insecure-deserializers-common-safe-to-suppress-md.md)]

## <a name="pseudo-code-examples"></a>의사 (pseudo) 코드 예제

### <a name="violation"></a>위반

```csharp
using System;
using System.IO;
using System.Runtime.Serialization.Formatters.Binary;

[Serializable]
public class BookRecord
{
    public string Title { get; set; }
    public string Author { get; set; }
    public int PageCount { get; set; }
    public AisleLocation Location { get; set; }
}

[Serializable]
public class AisleLocation
{
    public char Aisle { get; set; }
    public byte Shelf { get; set; }
}

public class ExampleClass
{
    public BookRecord DeserializeBookRecord(byte[] bytes)
    {
        BinaryFormatter formatter = new BinaryFormatter();
        using (MemoryStream ms = new MemoryStream(bytes))
        {
            return (BookRecord) formatter.Deserialize(ms);
        }
    }
}
```

```vb
Imports System
Imports System.IO
Imports System.Runtime.Serialization.Formatters.Binary

<Serializable()>
Public Class BookRecord
    Public Property Title As String
    Public Property Author As String
    Public Property Location As AisleLocation
End Class

<Serializable()>
Public Class AisleLocation
    Public Property Aisle As Char
    Public Property Shelf As Byte
End Class

Public Class ExampleClass
    Public Function DeserializeBookRecord(bytes As Byte()) As BookRecord
        Dim formatter As BinaryFormatter = New BinaryFormatter()
        Using ms As MemoryStream = New MemoryStream(bytes)
            Return CType(formatter.Deserialize(ms), BookRecord)
        End Using
    End Function
End Class
```

### <a name="solution"></a>솔루션

```csharp
using System;
using System.IO;
using System.Runtime.Serialization;
using System.Runtime.Serialization.Formatters.Binary;

public class BookRecordSerializationBinder : SerializationBinder
{
    public override Type BindToType(string assemblyName, string typeName)
    {
        // One way to discover expected types is through testing deserialization
        // of **valid** data and logging the types used.

        ////Console.WriteLine($"BindToType('{assemblyName}', '{typeName}')");

        if (typeName == "BookRecord" || typeName == "AisleLocation")
        {
            return null;
        }
        else
        {
            throw new ArgumentException("Unexpected type", nameof(typeName));
        }
    }
}

[Serializable]
public class BookRecord
{
    public string Title { get; set; }
    public string Author { get; set; }
    public int PageCount { get; set; }
    public AisleLocation Location { get; set; }
}

[Serializable]
public class AisleLocation
{
    public char Aisle { get; set; }
    public byte Shelf { get; set; }
}

public class ExampleClass
{
    public BookRecord DeserializeBookRecord(byte[] bytes)
    {
        BinaryFormatter formatter = new BinaryFormatter();
        formatter.Binder = new BookRecordSerializationBinder();
        using (MemoryStream ms = new MemoryStream(bytes))
        {
            return (BookRecord) formatter.Deserialize(ms);
        }
    }
}
```

```vb
Imports System
Imports System.IO
Imports System.Runtime.Serialization
Imports System.Runtime.Serialization.Formatters.Binary

Public Class BookRecordSerializationBinder
    Inherits SerializationBinder

    Public Overrides Function BindToType(assemblyName As String, typeName As String) As Type
        ' One way to discover expected types is through testing deserialization
        ' of **valid** data and logging the types used.

        'Console.WriteLine($"BindToType('{assemblyName}', '{typeName}')")

        If typeName = "BinaryFormatterVB.BookRecord" Or typeName = "BinaryFormatterVB.AisleLocation" Then
            Return Nothing
        Else
            Throw New ArgumentException("Unexpected type", NameOf(typeName))
        End If
    End Function
End Class

<Serializable()>
Public Class BookRecord
    Public Property Title As String
    Public Property Author As String
    Public Property Location As AisleLocation
End Class

<Serializable()>
Public Class AisleLocation
    Public Property Aisle As Char
    Public Property Shelf As Byte
End Class

Public Class ExampleClass
    Public Function DeserializeBookRecord(bytes As Byte()) As BookRecord
        Dim formatter As BinaryFormatter = New BinaryFormatter()
        formatter.Binder = New BookRecordSerializationBinder()
        Using ms As MemoryStream = New MemoryStream(bytes)
            Return CType(formatter.Deserialize(ms), BookRecord)
        End Using
    End Function
End Class
```

## <a name="related-rules"></a>관련된 규칙

[CA2300: 안전 하지 않은 deserializer BinaryFormatter를 사용 하지 마세요](ca2300-do-not-use-insecure-deserializer-binaryformatter.md)

[CA2302: BinaryFormatter.Binder BinaryFormatter.Deserialize를 호출 하기 전에 설정 되어 있는지 확인](ca2302-ensure-binaryformatter-binder-is-set-before-calling-binaryformatter-deserialize.md)