---
title: '워크플로 디자이너-방법: 이동 경로 탐색 사용'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 4a688056-37dc-406a-9071-be2141e192fe
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: de1004dd7a62fe4163147db4928783dd9a0dca98
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62949502"
---
# <a name="how-to-use-breadcrumb-navigation"></a>방법: 이동 경로 탐색 사용

세 가지 주요 워크플로 디자이너에 표시 되는 활동 집합을 변경 하려면:

1. 두 번 클릭하여 자식 활동으로 드릴인합니다.

2. 이동 경로 탐색 막대의 단추를 클릭하여 상위 활동으로 이동합니다.

3. 현재 위치의 활동을 확장하거나 축소합니다.

## <a name="using-breadcrumb-navigation"></a>이동 경로 탐색 사용

1. 클릭된 작업으로 루트 활동을 변경 하려면 워크플로 디자이너의 활동을 두 번 클릭 합니다. 클릭 한 활동이 루트에서 완전히 확장 한 다음 및 해당 상위 항목이 이동 경로 탐색 막대에 표시 됩니다. 이를 활동 드릴인/드릴아웃이라고도 합니다.

2. 현재 루트 활동의 상위 항목으로 이동하려면 이동 경로 탐색 막대에서 해당 활동을 클릭합니다.

## <a name="expanding-or-collapsing-an-activity-in-place"></a>현재 위치의 활동 확장 또는 축소

1. 활동의 갈매기형 펼침 단추를 클릭하면 현재 위치의 활동이 확장되거나 축소됩니다.

2. 이 단추를 클릭하여 확장 상태를 변경하면 확장의 새로운 상태가 XAML에 저장됩니다.

    > [!WARNING]
    > 일부 활동은 현재 위치에서 확장되지 않을 수도 있습니다. 현재 위치에서 활동을 확장할 수 없는 경우는 두 가지입니다. 즉, 활동의 부모가 현재 위치에서 자식을 확장하도록 허용하지 않는 경우(예: 순서도의 활동은 현재 위치에서 확장 불가능) 또는 활동 디자이너 자체에서 현재 위치에서의 확장을 허용하지 않는 경우입니다. 워크플로 디자이너에 포함 된 activity designer 중 두 번째 동작은 있지만 일부 사용자 지정 활동에는이 문제가 발생할 수 있습니다.

## <a name="expanding-all-or-collapsing-all-activities"></a>모든 활동 확장명 또는 축소

1. 사용 합니다 **모두 확장** 및 **모두 축소** 사용자 인터페이스를 확장 하거나 축소 하는 모든 현재 이동 경로 탐색 루트 아래에 있는 작업 단추입니다. 모두 확장 및 모두 축소는 전역 상태입니다. 즉, 이동 경로 탐색에서 모든 확장을 사용 하 여 루트 활동을 변경 하거나 모든 상태를 축소 하면 클릭할 때까지 유지 되도록 **복원**합니다.

2. 를 모든 확장을 적용 하거나 모든 상태를 축소 한 후을 클릭 합니다 **복원** 돌아가서 각 활동에 적용 되었던 상태를 보면에 나타나는 단추입니다.

    > [!WARNING]
    > 활동을 같은 <xref:System.Activities.Statements.Flowchart>, 제외 된 확장 위치에서 사용 하 여 연결 된 기능, 합니다 **모두 확장** 및 **모두 축소** 단추가 비활성화 됩니다는 **순서도**  디자이너입니다. 에 대 한 자세한 내용은 합니다 **순서도** 디자이너, 참조는 [순서도](../workflow-designer/flowchart-activity-designer.md) 항목입니다.

    > [!WARNING]
    > 모두 확장도 특별 한 영향을 주지 **스위치** 하 고 **TryCatch** activity designer입니다. 클릭 하면 **모두 확장**, 모든 switch case와 모든 try/catch/finally 블록에 표시 됩니다. 클릭 **복원** 하거나 **모두 축소** 는 개별 사례/블록의 내용을 보려면 클릭 수, 기본 상태로 이러한 디자이너를 반환 합니다.