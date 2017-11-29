---
title: "ISymUnmanagedVariable::GetAddressKind 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedVariable.GetAddressKind
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedVariable::GetAddressKind
helpviewer_keywords:
- GetAddressKind method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAddressKind method [.NET Framework debugging]
ms.assetid: a71563c0-62f2-4eb4-970c-825d61827613
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 930b55c98609e5f3bc33f30da766c4556fbe5512
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedvariablegetaddresskind-method"></a><span data-ttu-id="a062e-102">ISymUnmanagedVariable::GetAddressKind 方法</span><span class="sxs-lookup"><span data-stu-id="a062e-102">ISymUnmanagedVariable::GetAddressKind Method</span></span>
<span data-ttu-id="a062e-103">获取此变量的地址的种类。</span><span class="sxs-lookup"><span data-stu-id="a062e-103">Gets the kind of address of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a062e-104">语法</span><span class="sxs-lookup"><span data-stu-id="a062e-104">Syntax</span></span>  
  
```  
HRESULT GetAddressKind(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a062e-105">参数</span><span class="sxs-lookup"><span data-stu-id="a062e-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="a062e-106">[out]指向的指针`ULONG32`接收的值。</span><span class="sxs-lookup"><span data-stu-id="a062e-106">[out] A pointer to a `ULONG32` that receives the value.</span></span> <span data-ttu-id="a062e-107">可能的值定义在[CorSymAddrKind](../../../../docs/framework/unmanaged-api/diagnostics/corsymaddrkind-enumeration.md)枚举。</span><span class="sxs-lookup"><span data-stu-id="a062e-107">The possible values are defined in the [CorSymAddrKind](../../../../docs/framework/unmanaged-api/diagnostics/corsymaddrkind-enumeration.md) enumeration.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a062e-108">返回值</span><span class="sxs-lookup"><span data-stu-id="a062e-108">Return Value</span></span>  
 <span data-ttu-id="a062e-109">如果该方法成功; 则为 S_OK否则为 E_FAIL 或某些其他错误代码。</span><span class="sxs-lookup"><span data-stu-id="a062e-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a062e-110">要求</span><span class="sxs-lookup"><span data-stu-id="a062e-110">Requirements</span></span>  
 <span data-ttu-id="a062e-111">**标头：** CorSym.idl、 CorSym.h</span><span class="sxs-lookup"><span data-stu-id="a062e-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a062e-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a062e-112">See Also</span></span>  
 [<span data-ttu-id="a062e-113">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="a062e-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)