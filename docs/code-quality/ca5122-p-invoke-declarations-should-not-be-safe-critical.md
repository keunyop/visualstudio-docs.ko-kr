---
title: 'CA5122: P-Invoke 선언은 안전에 중요한 선언이 아니어야 합니다.'
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: f2581a6d-2a0e-40c1-b600-f5dc70909200
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9abe71337b5eb09d44ec6a244dc17e656768847a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62541053"
---
# <a name="ca5122-pinvoke-declarations-should-not-be-safe-critical"></a>CA5122 P/Invoke 선언은 안전에 중요한 선언이 아니어야 함

|||
|-|-|
|TypeName|PInvokesShouldNotBeSafeCriticalFxCopRule|
|CheckId|CA5122|
|범주|Microsoft.Security|
|변경 수준|주요 변경|

## <a name="cause"></a>원인
 P/Invoke 선언에 <xref:System.Security.SecuritySafeCriticalAttribute>가 표시되었습니다.

```csharp
[assembly: AllowPartiallyTrustedCallers]

// ...
public class C
{
    [SecuritySafeCritical]
    [DllImport("kernel32.dll")]
    public static extern bool Beep(int frequency, int duration); // CA5122 - safe critical p/invoke
   }
```

 이 예제에서 `C.Beep(...)`는 보안에 안전한 중요 메서드로 표시되었습니다.

## <a name="rule-description"></a>규칙 설명
 메서드는 보안에 중요한 작업을 수행할 때 SecuritySafeCritical로 표시되지만, 투명 코드에서도 안전하게 사용할 수 있습니다. 보안 투명성 모델의 기본 규칙 중 하나는 투명 코드가 P/Invoke를 통해 네이티브 코드를 절대 직접 호출할 수 없다는 점입니다. 따라서 P/Invoke를 SecuritySafeCritical로 표시할 경우 투명 코드가 P/Invoke를 호출할 수 없으며, 보안 분석에서 잘못 해석하는 원인이 됩니다.

## <a name="how-to-fix-violations"></a>위반 문제를 해결하는 방법
 투명 코드에서 P/Invoke를 사용할 수 있도록 만들려면 보안에 안전한 중요 래퍼 메서드를 노출하십시오.

```csharp
[assembly: AllowPartiallyTrustedCallers

class C
{
   [SecurityCritical]
   [DllImport("kernel32.dll", EntryPoint="Beep")]
   private static extern bool BeepPinvoke(int frequency, int duration); // Security Critical P/Invoke

   [SecuritySafeCritical]
   public static bool Beep(int frequency, int duration)
   {
      return BeepPInvoke(frequency, duration);
   }
}
```

## <a name="when-to-suppress-warnings"></a>경고를 표시 하는 경우
 이 규칙에서는 경고를 표시해야 합니다.