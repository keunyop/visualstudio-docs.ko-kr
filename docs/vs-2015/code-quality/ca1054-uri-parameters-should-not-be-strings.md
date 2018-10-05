---
title: 'CA1054: URI 매개 변수 안 문자열 | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- CA1054
- UriParametersShouldNotBeStrings
helpviewer_keywords:
- CA1054
- UriParametersShouldNotBeStrings
ms.assetid: 8e99d72b-a658-47a7-8dd5-9784ce2c30b8
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: f8fc894ae1f0db2f63161b3f3a9fbf0e875bbd96
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/24/2018
ms.locfileid: "47591275"
---
# <a name="ca1054-uri-parameters-should-not-be-strings"></a>CA1054: URI 매개 변수는 문자열이면 안 됩니다.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [CA1054: URI 매개 변수 문자열을 사용 하지 않아야](https://docs.microsoft.com/visualstudio/code-quality/ca1054-uri-parameters-should-not-be-strings)합니다.

|||
|-|-|
|TypeName|UriParametersShouldNotBeStrings|
|CheckId|CA1054|
|범주|Microsoft.Design|
|변경 수준|주요 변경|

## <a name="cause"></a>원인
 형식 이름에 "uri", "Uri", "urn", "Urn", "url" 또는 "Url" 포함 된 문자열 매개 변수를 사용 하 여 메서드를 선언 및 형식에는 해당 오버 로드를 선언 하지는 <xref:System.Uri?displayProperty=fullName> 매개 변수입니다.

## <a name="rule-description"></a>규칙 설명
 이 규칙 매개 변수 이름을 카멜식 대/소문자 규칙에 따라 토큰 나누고 각 토큰 "uri", "Uri", "urn", "Urn", "url" 또는 "Url"와 같은지 여부를 확인 합니다. 일치 하는 경우 규칙 매개 변수 uniform resource identifier (URI)를 나타낸다고 가정 합니다. URI의 문자열 표현은 구문 분석 및 인코딩 오류를 발생시키기 쉬우며 보안 문제를 일으킬 수 있습니다. URI의 문자열 표현을 사용 하는 메서드, 해당 오버 로드를 제공 해야의 인스턴스를 사용 하 여 <xref:System.Uri> 안전 하 고 안전한 방식으로 이러한 서비스를 제공 하는 클래스입니다.

## <a name="how-to-fix-violations"></a>위반 문제를 해결하는 방법
 이 규칙 위반을 해결 하려면 매개 변수를 변경 된 <xref:System.Uri> 형식 주요 변경 내용입니다. 또는 사용 하는 메서드의 오버 로드를 제공는 <xref:System.Uri> 매개 변수가이 주요 변경 내용입니다.

## <a name="when-to-suppress-warnings"></a>경고를 표시하지 않는 경우
 매개 변수는 URI를 나타내지 않는 경우이 규칙에서 경고를 표시 하지 않아도 안전 합니다.

## <a name="example"></a>예제
 다음 예제에서는 형식 `ErrorProne`, 형식 및이 규칙을 위반 하는 `SaferWay`, 규칙을 충족 하는 합니다.

 [!code-cpp[FxCop.Design.UriNotString#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.UriNotString/cpp/FxCop.Design.UriNotString.cpp#1)]
 [!code-csharp[FxCop.Design.UriNotString#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.UriNotString/cs/FxCop.Design.UriNotString.cs#1)]
 [!code-vb[FxCop.Design.UriNotString#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.UriNotString/vb/FxCop.Design.UriNotString.vb#1)]

## <a name="related-rules"></a>관련된 규칙
 [CA1056: URI 속성은 문자열이면 안 됩니다.](../code-quality/ca1056-uri-properties-should-not-be-strings.md)

 [CA1055: URI 반환 값은 문자열이면 안 됩니다.](../code-quality/ca1055-uri-return-values-should-not-be-strings.md)

 [CA2234: 문자열 대신 System.Uri 개체를 전달하십시오.](../code-quality/ca2234-pass-system-uri-objects-instead-of-strings.md)

 [CA1057: 문자열 URI 오버로드는 System.Uri 오버로드를 호출합니다.](../code-quality/ca1057-string-uri-overloads-call-system-uri-overloads.md)


