---
title: "ICLRTask2::EndPreventAsyncAbort 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRTask2.EndPreventAsyncAbort
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRTask2::EndPreventAsyncAbort
helpviewer_keywords:
- EndPreventAsyncAbort method [.NET Framework hosting]
- ICLRTask2::EndPreventAsyncAbort method [.NET Framework hosting]
ms.assetid: d8013659-e3df-44b3-814f-a6b534ce62f8
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c76a75004b4593e8e93aa4dd999c85c0fb7cf38a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="iclrtask2endpreventasyncabort-method"></a><span data-ttu-id="1fd9f-102">ICLRTask2::EndPreventAsyncAbort 方法</span><span class="sxs-lookup"><span data-stu-id="1fd9f-102">ICLRTask2::EndPreventAsyncAbort Method</span></span>
<span data-ttu-id="1fd9f-103">允许新的或挂起的线程中止请求导致线程中止当前线程上。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-103">Allows new or pending thread abort requests to result in thread aborts on the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1fd9f-104">语法</span><span class="sxs-lookup"><span data-stu-id="1fd9f-104">Syntax</span></span>  
  
```  
HRESULT EndPreventAsyncAbort();  
```  
  
## <a name="return-value"></a><span data-ttu-id="1fd9f-105">返回值</span><span class="sxs-lookup"><span data-stu-id="1fd9f-105">Return Value</span></span>  
 <span data-ttu-id="1fd9f-106">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-106">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="1fd9f-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1fd9f-107">HRESULT</span></span>|<span data-ttu-id="1fd9f-108">描述</span><span class="sxs-lookup"><span data-stu-id="1fd9f-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1fd9f-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="1fd9f-109">S_OK</span></span>|<span data-ttu-id="1fd9f-110">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-110">The method completed successfully.</span></span>|  
|<span data-ttu-id="1fd9f-111">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="1fd9f-111">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="1fd9f-112">这不是当前线程的线程上调用了方法。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-112">The method was called on a thread which is not the current thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1fd9f-113">备注</span><span class="sxs-lookup"><span data-stu-id="1fd9f-113">Remarks</span></span>  
 <span data-ttu-id="1fd9f-114">一个与当前线程调用此方法递减延迟线程中止计数器。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-114">Calling this method decrements the delay-thread-abort counter for the current thread by one.</span></span>  
  
 <span data-ttu-id="1fd9f-115">调用[iclrtask2:: Beginpreventasyncabort](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-beginpreventasyncabort-method.md)和`EndPreventAsyncAbort`可以嵌套。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-115">Calls to [ICLRTask2::BeginPreventAsyncAbort](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-beginpreventasyncabort-method.md) and `EndPreventAsyncAbort` can be nested.</span></span> <span data-ttu-id="1fd9f-116">只要计数器值大于零，当前线程的线程中止延迟。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-116">As long as the counter is greater than zero, thread aborts for the current thread are delayed.</span></span>  
  
 <span data-ttu-id="1fd9f-117">虚拟机 (VM) 内部使用此功能公开的功能。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-117">The functionality that is exposed by this feature is used internally by the virtual machine (VM).</span></span> <span data-ttu-id="1fd9f-118">不正确使用了这些方法可能导致虚拟机中未指定的行为。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-118">Misuse of these methods may cause unspecified behavior in the VM.</span></span> <span data-ttu-id="1fd9f-119">例如，调用`EndPreventAsyncAbort`而无需首先调用`BeginPreventAsyncAbort`VM 先前已增大时无法设置为零的计数器。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-119">For example, calling `EndPreventAsyncAbort` without first calling `BeginPreventAsyncAbort` could set the counter to zero when the VM has previously incremented it.</span></span> <span data-ttu-id="1fd9f-120">同样，内部计数器未检查存在溢出。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-120">Similarly, the internal counter is not checked for overflow.</span></span> <span data-ttu-id="1fd9f-121">如果该阈值超过其整型的限制，因为它就会递增主机和 VM，获得的行为是未指定。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-121">If it exceeds its integral limit because it is incremented by both the host and the VM, the resulting behavior is unspecified.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1fd9f-122">要求</span><span class="sxs-lookup"><span data-stu-id="1fd9f-122">Requirements</span></span>  
 <span data-ttu-id="1fd9f-123">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1fd9f-124">**标头：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1fd9f-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1fd9f-125">**库：**作为 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="1fd9f-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1fd9f-126">**.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1fd9f-126">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1fd9f-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1fd9f-127">See Also</span></span>  
 [<span data-ttu-id="1fd9f-128">BeginPreventAsyncAbort 方法</span><span class="sxs-lookup"><span data-stu-id="1fd9f-128">BeginPreventAsyncAbort Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-beginpreventasyncabort-method.md)  
 [<span data-ttu-id="1fd9f-129">ICLRTask2 接口</span><span class="sxs-lookup"><span data-stu-id="1fd9f-129">ICLRTask2 Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-interface.md)  
 [<span data-ttu-id="1fd9f-130">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="1fd9f-130">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="1fd9f-131">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="1fd9f-131">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="1fd9f-132">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="1fd9f-132">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)  
 [<span data-ttu-id="1fd9f-133">承载接口</span><span class="sxs-lookup"><span data-stu-id="1fd9f-133">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)