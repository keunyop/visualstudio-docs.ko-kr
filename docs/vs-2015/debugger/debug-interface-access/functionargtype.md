---
title: FunctionArgType | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- FunctionArgType symbol
ms.assetid: 9f072fd3-0b99-405c-af99-fd44cd56fd73
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 96f816ff40b40f0de6b6f828996a64407b88f04e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "58984160"
---
# <a name="functionargtype"></a>FunctionArgType
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

함수의 각 매개 변수에 의해 식별 되는 `SymTagFunctionArgType` 기호입니다.  
  
## <a name="properties"></a>속성  
 다음 표에서이 기호 형식에 대 한 추가 올바른 속성을 보여 줍니다.  
  
|속성|데이터 형식|설명|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_classParent](../../debugger/debug-interface-access/idiasymbol-get-classparent.md)|`IDiaSymbol*`|FunctionType 부모에 대 한 기호입니다.|  
|[IDiaSymbol::get_classParentId](../../debugger/debug-interface-access/idiasymbol-get-classparentid.md)|`DWORD`|ID 클래스 부모 기호입니다.|  
|[IDiaSymbol::get_lexicalParent](../../debugger/debug-interface-access/idiasymbol-get-lexicalparent.md)|`IDiaSymbol*`|기호 묶는 [Compiland](../../debugger/debug-interface-access/compiland.md)합니다.|  
|[IDiaSymbol::get_lexicalParentId](../../debugger/debug-interface-access/idiasymbol-get-lexicalparentid.md)|`DWORD`|어휘 부모 기호 ID입니다.|  
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol-get-symindexid.md)|`DWORD`|기호 인덱스 ID입니다.|  
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol-get-symtag.md)|`DWORD`|반환 `SymTagFunctionArgType` (중 하나는 [SymTagEnum 열거형](../../debugger/debug-interface-access/symtagenum.md) 값).|  
|[IDiaSymbol::get_type](../../debugger/debug-interface-access/idiasymbol-get-type.md)|`IDiaSymbol*`|매개 변수의 형식입니다.|  
|[IDiaSymbol::get_typeId](../../debugger/debug-interface-access/idiasymbol-get-typeid.md)|`DWORD`|ID 형식 기호입니다.|  
  
## <a name="see-also"></a>참고 항목  
 [기호 형식의 클래스 계층 구조](../../debugger/debug-interface-access/class-hierarchy-of-symbol-types.md)   
 [FunctionType](../../debugger/debug-interface-access/functiontype.md)
