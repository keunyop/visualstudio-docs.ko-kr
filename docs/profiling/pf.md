---
title: PF | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: cdc0a094-a986-4629-bd1c-dd5fdca323dc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bf6bc8ae841ad8ba0d3fd376176bdff2332fb958
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63431999"
---
# <a name="pf"></a>PF
*VSPerfCmd.exe* **PF** 옵션은 페이지 폴트로 샘플링되는 프로파일링 이벤트를 설정하고 경우에 따라 샘플링 간격의 페이지 폴트 수를 기본값 10에서 변경합니다.

> [!NOTE]
> **PF**는 64비트 시스템에서 사용할 수 없습니다.

**PF**는 **Launch** 또는 **Attach** 옵션도 포함하는 명령줄에서만 사용할 수 있습니다.

 기본적으로 샘플링 이벤트는 무중단 프로세서 클록 주기로 설정되어 있고 샘플링 간격은 10,000,000으로 설정되어 있습니다. **Timer**, **PF**, **Sys** 및 **Counter** 옵션을 사용하여 샘플 이벤트와 샘플링 간격을 설정할 수 있습니다. **GC** 옵션은 각 할당 및 가비지 컬렉션 이벤트에서 .NET 메모리 데이터를 수집합니다. 명령줄에서는 이러한 옵션 중 하나만 지정할 수 있습니다.

 샘플링 이벤트와 샘플링 간격은 **Launch** 또는 **Attach** 옵션이 포함된 첫 번째 명령줄에서만 설정할 수 있습니다.

## <a name="syntax"></a>구문

```cmd
VSPerfCmd.exe {/Launch:AppName|/Attach:PID} /PF[:Events] [Options]
```

#### <a name="parameters"></a>매개 변수
 `Events` 샘플링 간격에서 페이지 폴트 이벤트 수를 지정하는 정수 값입니다. `Events`를 지정하지 않으면 간격은 10으로 설정됩니다.

## <a name="required-options"></a>필수 옵션
 **PF**는 다음 옵션 중 하나가 포함된 명령줄에서만 지정할 수 있습니다.

 **시작:** `AppName` 프로파일러 및 AppName에서 지정한 애플리케이션을 시작합니다.

 **연결:** `PID` AppName으로 지정한 프로세스에 프로파일러를 연결합니다.

## <a name="invalid-options"></a>잘못된 옵션
 다음 옵션은 **PF**와 동일한 명령줄에서 지정할 수 없습니다.

 **Timer**[**:**`Cycles`] 샘플링 이벤트를 프로세서 클록 주기로 설정하고 경우에 따라 샘플링 간격을 `Cycles`로 설정합니다. 기본 타이머 간격은 10,000,000입니다.

 **Sys**[**:**`Events`] 프로파일링된 애플리케이션에서 호출에 대한 샘플링 이벤트를 운영 체제 커널(syscall)로 설정하고 필요에 따라 샘플링 간격을 `Events`로 설정합니다. 기본 시스템 간격은 10입니다.

 **Counter:** `Name`[`,Reload`[`,FriendlyName`]] 샘플링 이벤트를 `Name`으로 지정한 CPU 성능 카운터로 설정하고 샘플링 간격을 `Reload`로 설정합니다.

 **GC**[**:**{**Allocation**&#124;**Lifetime**}] .NET 메모리 데이터를 수집합니다. 기본적으로(**Allocation**) 모든 메모리 할당 이벤트에서 데이터가 수집됩니다. **Lifetime** 매개변수가 지정되면 데이터는 각 가비지 컬렉션 이벤트에서도 수집됩니다.

## <a name="example"></a>예제
 이 예제는 프로파일링 샘플 이벤트를 페이지 폴트로 설정하고 샘플링 간격을 20 페이지 폴트로 설정하는 방법을 보여 줍니다.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp
VSPerfCmd.exe /Launch:TestApp.exe /PF:20
```

## <a name="see-also"></a>참고 항목
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [독립 실행형 애플리케이션 프로파일링](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [ASP.NET 웹 애플리케이션 프로파일링](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [서비스 프로파일링](../profiling/command-line-profiling-of-services.md)