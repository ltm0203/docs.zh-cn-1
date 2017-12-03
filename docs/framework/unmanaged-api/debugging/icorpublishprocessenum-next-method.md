---
title: "ICorPublishProcessEnum::Next 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorPublishProcessEnum.Next
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorPublishProcessEnum::Next
helpviewer_keywords:
- ICorPublishProcessEnum::Next method [.NET Framework debugging]
- Next method, ICorPublishProcessEnum interface [.NET Framework debugging]
ms.assetid: 6c399f37-1e38-4ca1-b70d-8ae41f7228b7
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 6823a8d973b997576da3271c85234b347f1c8562
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="icorpublishprocessenumnext-method"></a><span data-ttu-id="4cf8b-102">ICorPublishProcessEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="4cf8b-102">ICorPublishProcessEnum::Next Method</span></span>
<span data-ttu-id="4cf8b-103">从开始在当前光标位置处的集合获取指定的数目的进程。</span><span class="sxs-lookup"><span data-stu-id="4cf8b-103">Gets the specified number of processes from the collection, starting at the current cursor position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4cf8b-104">语法</span><span class="sxs-lookup"><span data-stu-id="4cf8b-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorPublishProcess **objects,  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4cf8b-105">参数</span><span class="sxs-lookup"><span data-stu-id="4cf8b-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="4cf8b-106">[in]要检索的进程数。</span><span class="sxs-lookup"><span data-stu-id="4cf8b-106">[in] The number of processes to be retrieved.</span></span>  
  
 `objects`  
 <span data-ttu-id="4cf8b-107">[out]检索到的数组的指针[ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)对象，其中每个表示的进程。</span><span class="sxs-lookup"><span data-stu-id="4cf8b-107">[out] A pointer to the array of retrieved [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) objects, each of which represents a process.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="4cf8b-108">[out]指向实际返回的进程数。</span><span class="sxs-lookup"><span data-stu-id="4cf8b-108">[out] Pointer to the number of processes actually returned.</span></span> <span data-ttu-id="4cf8b-109">此值可能为 null 如果`celt`是之一。</span><span class="sxs-lookup"><span data-stu-id="4cf8b-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4cf8b-110">要求</span><span class="sxs-lookup"><span data-stu-id="4cf8b-110">Requirements</span></span>  
 <span data-ttu-id="4cf8b-111">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4cf8b-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4cf8b-112">**标头：** CorPub.idl、 CorPub.h</span><span class="sxs-lookup"><span data-stu-id="4cf8b-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="4cf8b-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4cf8b-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4cf8b-114">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4cf8b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4cf8b-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4cf8b-115">See Also</span></span>  
 [<span data-ttu-id="4cf8b-116">ICorPublishProcessEnum 接口</span><span class="sxs-lookup"><span data-stu-id="4cf8b-116">ICorPublishProcessEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md)