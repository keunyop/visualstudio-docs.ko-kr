---
title: 코드 메트릭 계산
ms.date: 11/02/2018
ms.topic: conceptual
helpviewer_keywords:
- code metrics [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f989e5ec028f3a296585c54eb17b54f4da7c1cf0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62809317"
---
# <a name="code-metrics-values"></a>코드 메트릭 값

최신 소프트웨어 응용 프로그램의 복잡성이 높아 안정적이 고 유지 관리 가능한 코드 만들기가 늘어납니다. 코드 메트릭은 개발자가 개발 중인 코드에 대해 더 정확히 파악할 수 있도록 하는 소프트웨어 측정 방법입니다. 코드 메트릭을 활용 하 여 개발자는 형식 및/또는 메서드는 수정 하거나 더 철저 하 게 테스트를 파악할 수 있습니다. 개발 팀은 잠재적 위험을 식별 하 고 프로젝트의 현재 상태를 이해 하 고 소프트웨어 개발 하는 동안 진행률을 추적할 수 있습니다.

개발자는 복잡 하 고 관리 코드의 유지 관리 편의성을 측정 하는 코드 메트릭 데이터를 생성 하려면 Visual Studio를 사용할 수 있습니다. 전체 솔루션 또는 단일 프로젝트에 대해 코드 메트릭 데이터를 생성할 수 있습니다.

Visual Studio에서 코드 메트릭 데이터를 생성 하는 방법에 대 한 정보를 참조 하세요. [방법: 코드 메트릭 데이터 생성](../code-quality/how-to-generate-code-metrics-data.md)합니다.

## <a name="software-measurements"></a>소프트웨어 측정

다음은 코드를 Visual Studio를 계산 하는 메트릭 결과 보여 줍니다.

- **유지 관리 인덱스** -코드를 유지 하는 상대적인 편의성을 나타내는 0과 100 사이의 인덱스 값을 계산 합니다. 값이 높으면 더 나은 유지 관리를 의미합니다. 코드에서 문제점을 신속 하 게 식별 하 색으로 구분 된 등급을 사용할 수 있습니다. 녹색 등급 20과 100 사이의 이며 코드에 적절 한 유지 관리에 있음을 나타냅니다. 노란색 등급 10에서 19 사이의 약간 유지 관리 가능한 코드를 나타냅니다. 빨간색 등급을 0에서 9 사이의 등급을 낮은 유지 관리를 나타냅니다.

- **순환 복잡성** -코드의 구조적 복잡성을 측정 합니다. 프로그램 흐름에 다른 코드 경로 수를 계산 하 여 생성 됩니다. 복잡 한 제어 흐름에 있는 프로그램 좋은 코드 검사를 위해 더 많은 테스트 해야 하 고 줄이려면 됩니다.

- **상속 수준** -클래스 계층 구조의 루트를 확장 하는 클래스 정의의 수를 나타냅니다. 더 깊게 계층 더 어렵게 특정 메서드 및 필드 정의 이해 하는 것 또는 / 및 재정의 합니다.

- **클래스 결합** -매개 변수, 지역 변수, 반환 형식, 메서드 호출, 제네릭 또는 템플릿 인스턴스화, 기본 클래스, 인터페이스 구현, 외부 형식에 정의 된 필드를 통해 고유한 클래스 결합을 측정 하 고 특성 장식 합니다. 좋은 소프트웨어 설계는 형식 및 메서드 높은 응집력 및 있어야 결합 부족을 나타냅니다. 높은 결합 다시 사용 하 고 다른 형식에는 많은 상호 종속성으로 인해 유지 관리 하기 어려울 정도로 디자인을 나타냅니다.

- **줄의 코드로** -코드에서 줄의 대략적인 수를 나타냅니다. 수 IL 코드를 기반으로 하며 되지 않으므로 소스 코드 파일에서 줄의 정확한 수를 너무 많은 작업을 수행 하려고 하는 형식 또는 메서드 및 서로 분리 해야 매우 높은 수를 나타낼 수 있습니다. 또한 형식 또는 메서드가 유지 관리 하기가 수 있습니다 나타낼 수 있습니다.

   > [!NOTE]
   > 합니다 [명령줄 버전](../code-quality/how-to-generate-code-metrics-data.md#command-line-code-metrics) 코드 메트릭 도구 계산 코드의 실제 줄 IL 대신 소스 코드를 분석 하므로 합니다.

## <a name="anonymous-methods"></a>무명 메서드

*무명 메서드* 는 이름이 없는 메서드입니다. 무명 메서드 코드 블록을 대리자 매개 변수로 전달 하도록 가장 자주 사용 됩니다. 메트릭 결과 무명 메서드의 메서드 또는 접근자와 같은 멤버에 선언 된 메서드를 선언 하는 멤버와 연결 됩니다. 메서드를 호출 하는 멤버와 연결 되지 않습니다.

코드 메트릭 무명 메서드를 처리 하는 방법에 대 한 자세한 내용은 참조 하세요. [무명 메서드 및 코드 분석](../code-quality/anonymous-methods-and-code-analysis.md)합니다.

## <a name="generated-code"></a>생성 된 코드

일부 소프트웨어 도구 및 컴파일러에는 프로젝트에 추가 되 고 프로젝트 개발자 보이지 않는 하거나 변경 하지 않아야 하는 코드를 생성 합니다. 주로 코드 메트릭을 메트릭 값을 계산할 때 생성 된 코드를 무시 합니다. 따라서 새로운 개발자 보고 변경할 수 있는 반영 하도록 메트릭 값을 수 있습니다.

Windows Forms에 대 한 생성 된 코드는 개발자 보고 변경할 수 있는 코드 이기 때문에 무시 되지 않습니다.

## <a name="next-steps"></a>다음 단계

- [방법: 코드 메트릭 데이터 생성](../code-quality/how-to-generate-code-metrics-data.md)
- [코드 메트릭 결과 창 사용](../code-quality/working-with-code-metrics-data.md)