---
title: EXCEPTION_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- EXCEPTION_INFO
helpviewer_keywords:
- EXCEPTION_INFO structure
ms.assetid: d046957a-b97d-420b-b46b-c67cbaef709e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4c5863c9ebb790ebcbc267f62cc2a0a1fd14603c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56686264"
---
# <a name="exceptioninfo"></a>EXCEPTION_INFO
디버그 중인 프로그램에서 throw 된 런타임 오류 또는 예외를 설명 합니다.

## <a name="syntax"></a>구문

```cpp
typedef struct tagEXCEPTION_INFO {
    IDebugProgram2* pProgram;
    BSTR            bstrProgramName;
    BSTR            bstrExceptionName;
    DWORD           dwCode;
    EXCEPTION_STATE dwState;
    GUID            guidType;
} EXCEPTION_INFO;
```

```csharp
public struct EXCEPTION_INFO {
    public IDebugProgram2 pProgram;
    public string         bstrProgramName;
    public string         bstrExceptionName;
    public uint           dwCode;
    public uint           dwState;
    public Guid           guidType;
};
```

## <a name="members"></a>멤버
pProgram 합니다 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) 예외가 발생 한 프로그램을 나타내는 개체입니다.

프로그램의 이름 bstrProgramName에서 예외가 발생 합니다.

예외의 이름 bstrExceptionName입니다.

dwCode 예외 또는 런타임 오류에 대 한 식별 코드입니다.

dwState는 값을 [EXCEPTION_STATE](../../../extensibility/debugger/reference/exception-state.md) 예외 상태를 정의 하는 열거형입니다.

guidType GUID 언어 식별자를 `guidLang` 또는 `guidEng`합니다.

## <a name="remarks"></a>설명
이 구조에 대 한 매개 변수로 전달 되는 [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md) 하며 [RemoveSetException](../../../extensibility/debugger/reference/idebugengine2-removesetexception.md) 메서드. 이 구조에 전달 되는 [GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md) 채워야 하는 방법입니다.

## <a name="requirements"></a>요구 사항
헤더: msdbg.h

네임스페이스: Microsoft.VisualStudio.Debugger.Interop

어셈블리: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>참고 항목
- [클래스 및 공용 구조체](../../../extensibility/debugger/reference/structures-and-unions.md)
- [EXCEPTION_STATE](../../../extensibility/debugger/reference/exception-state.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md)
- [RemoveSetException](../../../extensibility/debugger/reference/idebugengine2-removesetexception.md)
- [GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md)
