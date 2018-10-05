---
title: 'CA1059: 멤버는 구체적인 특정 형식을 노출 하지 | Microsoft Docs'
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
- CA1059
- MembersShouldNotExposeCertainConcreteTypes
helpviewer_keywords:
- MembersShouldNotExposeCertainConcreteTypes
- CA1059
ms.assetid: 59f61f52-8d6c-49cb-aefb-191910523a3c
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 073d55a9a5ae6caa573a2c3db282aaa5e5ea4e57
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/24/2018
ms.locfileid: "47591979"
---
# <a name="ca1059-members-should-not-expose-certain-concrete-types"></a>CA1059: 멤버는 구체적인 특정 형식을 노출하면 안 됩니다.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [CA1059: 멤버 구체적인 특정 형식을 노출 하면 안](https://docs.microsoft.com/visualstudio/code-quality/ca1059-members-should-not-expose-certain-concrete-types)합니다.

|||
|-|-|
|TypeName|MembersShouldNotExposeCertainConcreteTypes|
|CheckId|CA1059|
|범주|Microsoft.Design|
|변경 수준|주요 변경|

## <a name="cause"></a>원인
 외부에서 볼 수 있는 멤버는 구체적인 특정 형식을 해당 매개 변수 중 하나를 통해 구체적인 특정 형식을 노출 또는 값을 반환 합니다. 현재이 규칙은 구체적인 형식은 노출을 보고:

-   파생 된 형식 <xref:System.Xml.XmlNode?displayProperty=fullName>합니다.

## <a name="rule-description"></a>규칙 설명
 구체적인 형식은 완전히 구현되었기 때문에 인스턴스화할 수 있는 형식을 말합니다. 멤버의 광범위 하 게 사용할 수 있도록, 하려면 구체적인 형식을 제안 된 인터페이스로 바꿉니다. 이 멤버를 인터페이스를 구현 하는 형식 그대로 사용 하거나 인터페이스를 구현 하는 형식이 필요한 경우 사용할 수 있습니다.

 다음 표에서 대상된 구체적인 형식 및 해당 제안 된 대체 합니다.

|구체적인 형식|Replacement|
|-------------------|-----------------|
|<xref:System.Xml.XPath.XPathDocument>|<xref:System.Xml.XPath.IXPathNavigable?displayProperty=fullName>.<br /><br /> 인터페이스를 사용 하 여 XML 데이터 원본의 특정 구현에서 멤버를 분리 합니다.|

## <a name="how-to-fix-violations"></a>위반 문제를 해결하는 방법
 이 규칙 위반 문제를 해결 하려면 구체적인 형식을 제안 된 인터페이스로 변경 합니다.

## <a name="when-to-suppress-warnings"></a>경고를 표시하지 않는 경우
 구체적인 형식에서 제공 하는 특정 기능이 필요한 경우이 규칙에서 메시지를 표시 하지 않으려면 안전 합니다.

## <a name="related-rules"></a>관련된 규칙
 [CA1011: 기본 형식을 매개 변수로 전달해 보십시오.](../code-quality/ca1011-consider-passing-base-types-as-parameters.md)


