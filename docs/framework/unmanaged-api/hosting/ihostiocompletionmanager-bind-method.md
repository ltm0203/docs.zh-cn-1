---
title: "IHostIoCompletionManager::Bind 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostIoCompletionManager.Bind
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostIoCompletionManager::Bind
helpviewer_keywords:
- IHostIoCompletionManager::Bind method [.NET Framework hosting]
- Bind method [.NET Framework hosting]
ms.assetid: acd74cb5-7e22-4a07-83c3-82288e1abd9f
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d5eba258065c5ddbbf6fad474aed700065b155a4
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="ihostiocompletionmanagerbind-method"></a><span data-ttu-id="9312c-102">IHostIoCompletionManager::Bind 方法</span><span class="sxs-lookup"><span data-stu-id="9312c-102">IHostIoCompletionManager::Bind Method</span></span>
<span data-ttu-id="9312c-103">将指定的句柄绑定到 I/O 完成端口已创建的以前调用[CreateIoCompletionPort](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-createiocompletionport-method.md)。</span><span class="sxs-lookup"><span data-stu-id="9312c-103">Binds the specified handle to an I/O completion port that has been created by an earlier call to [CreateIoCompletionPort](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-createiocompletionport-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9312c-104">语法</span><span class="sxs-lookup"><span data-stu-id="9312c-104">Syntax</span></span>  
  
```  
HRESULT Bind (  
    [in] HANDLE hPort,  
    [in] HANDLE hHandle  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9312c-105">参数</span><span class="sxs-lookup"><span data-stu-id="9312c-105">Parameters</span></span>  
 `hPort`  
 <span data-ttu-id="9312c-106">[in]要将绑定到 I/O 完成端口`hHandle`。</span><span class="sxs-lookup"><span data-stu-id="9312c-106">[in] The I/O completion port to which to bind `hHandle`.</span></span> <span data-ttu-id="9312c-107">如果值`hPort`为 null，`hHandle`绑定到默认 I/O 完成端口。</span><span class="sxs-lookup"><span data-stu-id="9312c-107">If the value of `hPort` is null, `hHandle` is bound to the default I/O completion port.</span></span>  
  
 `hHandle`  
 <span data-ttu-id="9312c-108">[in]若要将绑定到的操作系统句柄`hPort`。</span><span class="sxs-lookup"><span data-stu-id="9312c-108">[in] The operating system handle to bind to `hPort`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9312c-109">返回值</span><span class="sxs-lookup"><span data-stu-id="9312c-109">Return Value</span></span>  
  
|<span data-ttu-id="9312c-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9312c-110">HRESULT</span></span>|<span data-ttu-id="9312c-111">描述</span><span class="sxs-lookup"><span data-stu-id="9312c-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9312c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9312c-112">S_OK</span></span>|<span data-ttu-id="9312c-113">`Bind`已成功返回。</span><span class="sxs-lookup"><span data-stu-id="9312c-113">`Bind` returned successfully.</span></span>|  
|<span data-ttu-id="9312c-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="9312c-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="9312c-115">公共语言运行时 (CLR) 尚未加载到进程中，或 CLR 处于不能运行托管的代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="9312c-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="9312c-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="9312c-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="9312c-117">调用操作已超时。</span><span class="sxs-lookup"><span data-stu-id="9312c-117">The call timed out.</span></span>|  
|<span data-ttu-id="9312c-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="9312c-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="9312c-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="9312c-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="9312c-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="9312c-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="9312c-121">事件已被取消时被阻塞的线程，或者纤程正在等待它。</span><span class="sxs-lookup"><span data-stu-id="9312c-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="9312c-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="9312c-122">E_FAIL</span></span>|<span data-ttu-id="9312c-123">出现未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="9312c-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="9312c-124">如果某方法返回 E_FAIL，CLR 不再可用进程内。</span><span class="sxs-lookup"><span data-stu-id="9312c-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="9312c-125">到托管方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="9312c-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9312c-126">备注</span><span class="sxs-lookup"><span data-stu-id="9312c-126">Remarks</span></span>  
 <span data-ttu-id="9312c-127">通过调用创建 I/O 完成端口`CreateIoCompletionPort`。</span><span class="sxs-lookup"><span data-stu-id="9312c-127">An I/O completion port is created by using a call to `CreateIoCompletionPort`.</span></span> <span data-ttu-id="9312c-128">CLR 调用`Bind`将句柄绑定到该端口。</span><span class="sxs-lookup"><span data-stu-id="9312c-128">The CLR calls `Bind` to bind a handle to that port.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9312c-129">完成的 I/O 请求后，宿主必须调用[iclriocompletionmanager:: Oncomplete](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="9312c-129">When an I/O request completes, the host must call the [ICLRIoCompletionManager::OnComplete](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9312c-130">要求</span><span class="sxs-lookup"><span data-stu-id="9312c-130">Requirements</span></span>  
 <span data-ttu-id="9312c-131">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9312c-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9312c-132">**标头：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="9312c-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9312c-133">**库：**作为 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="9312c-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9312c-134">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9312c-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9312c-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9312c-135">See Also</span></span>  
 [<span data-ttu-id="9312c-136">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="9312c-136">ICLRIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md)