---
title: "ICorConfiguration::SetDebuggerThreadControl 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorConfiguration.SetDebuggerThreadControl
api_location: mscoree.dll
api_type: COM
f1_keywords: SetDebuggerThreadControl
helpviewer_keywords:
- SetDebuggerThreadControl method [.NET Framework hosting]
- ICorConfiguration::SetDebuggerThreadControl method [.NET Framework hosting]
ms.assetid: 1ded7639-dacb-4db1-961c-d1ceaec01959
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 4716e814c352fceacd8b949c2670058cf8a03bf1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="icorconfigurationsetdebuggerthreadcontrol-method"></a><span data-ttu-id="411e8-102">ICorConfiguration::SetDebuggerThreadControl 方法</span><span class="sxs-lookup"><span data-stu-id="411e8-102">ICorConfiguration::SetDebuggerThreadControl Method</span></span>
<span data-ttu-id="411e8-103">设置调试服务将调用公共语言运行时 (CLR) 线程阻止和解除阻止以用于调试的回调接口。</span><span class="sxs-lookup"><span data-stu-id="411e8-103">Sets the callback interface that the debugging services will call as common language runtime (CLR) threads are blocked and unblocked for debugging.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="411e8-104">语法</span><span class="sxs-lookup"><span data-stu-id="411e8-104">Syntax</span></span>  
  
```  
HRESULT SetDebuggerThreadControl (  
    [in] IDebuggerThreadControl* pDebuggerThreadControl  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="411e8-105">参数</span><span class="sxs-lookup"><span data-stu-id="411e8-105">Parameters</span></span>  
 `pDebuggerThreadControl`  
 <span data-ttu-id="411e8-106">[in]指向的指针[IDebuggerThreadControl](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-interface.md)通知主机有关阻止和取消阻止的线程调试服务的对象。</span><span class="sxs-lookup"><span data-stu-id="411e8-106">[in] A pointer to an [IDebuggerThreadControl](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-interface.md) object that notifies the host about the blocking and unblocking of threads by the debugging services.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="411e8-107">要求</span><span class="sxs-lookup"><span data-stu-id="411e8-107">Requirements</span></span>  
 <span data-ttu-id="411e8-108">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="411e8-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="411e8-109">**标头：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="411e8-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="411e8-110">**库：**作为 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="411e8-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="411e8-111">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="411e8-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="411e8-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="411e8-112">See Also</span></span>  
 [<span data-ttu-id="411e8-113">ICorConfiguration 接口</span><span class="sxs-lookup"><span data-stu-id="411e8-113">ICorConfiguration Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)