---
title: "ICorDebugAppDomain 接口 1"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugAppDomain
api_location: corguids.lib
api_type: COM
f1_keywords: ICorDebugAppDomain
helpviewer_keywords: ICorDebugAppDomain interface [.NET Framework debugging]
ms.assetid: be7ae711-1217-4a44-be40-166e29641b77
topic_type: apiref
caps.latest.revision: "22"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 19cf38920ed818dfbba9cd83bd64fdc408281e0b
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugappdomain-interface1"></a><span data-ttu-id="4a8fc-102">ICorDebugAppDomain 接口 1</span><span class="sxs-lookup"><span data-stu-id="4a8fc-102">ICorDebugAppDomain Interface1</span></span>
<span data-ttu-id="4a8fc-103">提供用于调试应用程序域的方法。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-103">Provides methods for debugging application domains.</span></span> <span data-ttu-id="4a8fc-104">此接口是 ICorDebugController 的子类。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-104">This interface is a subclass of ICorDebugController.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4a8fc-105">方法</span><span class="sxs-lookup"><span data-stu-id="4a8fc-105">Methods</span></span>  
  
|<span data-ttu-id="4a8fc-106">方法</span><span class="sxs-lookup"><span data-stu-id="4a8fc-106">Method</span></span>|<span data-ttu-id="4a8fc-107">描述</span><span class="sxs-lookup"><span data-stu-id="4a8fc-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4a8fc-108">Attach 方法</span><span class="sxs-lookup"><span data-stu-id="4a8fc-108">Attach Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-attach-method.md)|<span data-ttu-id="4a8fc-109">将调试器附加到应用程序域。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-109">Attaches the debugger to the application domain.</span></span>|  
|[<span data-ttu-id="4a8fc-110">EnumerateAssemblies 方法</span><span class="sxs-lookup"><span data-stu-id="4a8fc-110">EnumerateAssemblies Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-enumerateassemblies-method.md)|<span data-ttu-id="4a8fc-111">应用程序域中获取程序集的枚举数。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-111">Gets an enumerator for the assemblies in the application domain.</span></span>|  
|[<span data-ttu-id="4a8fc-112">EnumerateBreakpoints 方法</span><span class="sxs-lookup"><span data-stu-id="4a8fc-112">EnumerateBreakpoints Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-enumeratebreakpoints-method.md)|<span data-ttu-id="4a8fc-113">应用程序域中获取所有活动断点的枚举数。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-113">Gets an enumerator for all active breakpoints in the application domain.</span></span>|  
|[<span data-ttu-id="4a8fc-114">EnumerateSteppers 方法</span><span class="sxs-lookup"><span data-stu-id="4a8fc-114">EnumerateSteppers Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-enumeratesteppers-method.md)|<span data-ttu-id="4a8fc-115">应用程序域中获取所有活动分档的枚举数。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-115">Gets an enumerator for all active steppers in the application domain.</span></span>|  
|[<span data-ttu-id="4a8fc-116">GetId 方法</span><span class="sxs-lookup"><span data-stu-id="4a8fc-116">GetId Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-getid-method.md)|<span data-ttu-id="4a8fc-117">获取应用程序域的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-117">Gets the unique ID of the application domain.</span></span>|  
|[<span data-ttu-id="4a8fc-118">GetModuleFromMetaDataInterface 方法</span><span class="sxs-lookup"><span data-stu-id="4a8fc-118">GetModuleFromMetaDataInterface Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-getmodulefrommetadatainterface-method.md)|<span data-ttu-id="4a8fc-119">获取给定元数据接口的 icor 调试模块对象。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-119">Gets the ICorDebugModule object with the given metadata interface.</span></span>|  
|[<span data-ttu-id="4a8fc-120">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="4a8fc-120">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-getname-method.md)|<span data-ttu-id="4a8fc-121">获取应用程序域的名称。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-121">Gets the name of the application domain.</span></span>|  
|[<span data-ttu-id="4a8fc-122">GetObject 方法</span><span class="sxs-lookup"><span data-stu-id="4a8fc-122">GetObject Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-getobject-method.md)|<span data-ttu-id="4a8fc-123">公共语言运行时 (CLR) 应用程序域中获取的接口指针。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-123">Gets an interface pointer to the common language runtime (CLR) application domain.</span></span>|  
|[<span data-ttu-id="4a8fc-124">GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="4a8fc-124">GetProcess Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-getprocess-method.md)|<span data-ttu-id="4a8fc-125">获取包含应用程序域的进程。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-125">Gets the process containing the application domain.</span></span>|  
|[<span data-ttu-id="4a8fc-126">IsAttached 方法</span><span class="sxs-lookup"><span data-stu-id="4a8fc-126">IsAttached Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-isattached-method.md)|<span data-ttu-id="4a8fc-127">确定是否将调试器附加到应用程序域。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-127">Determines whether the debugger is attached to the application domain.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4a8fc-128">备注</span><span class="sxs-lookup"><span data-stu-id="4a8fc-128">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4a8fc-129">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-129">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4a8fc-130">要求</span><span class="sxs-lookup"><span data-stu-id="4a8fc-130">Requirements</span></span>  
 <span data-ttu-id="4a8fc-131">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4a8fc-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a8fc-132">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4a8fc-132">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4a8fc-133">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4a8fc-133">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4a8fc-134">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4a8fc-134">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a8fc-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4a8fc-135">See Also</span></span>  
 [<span data-ttu-id="4a8fc-136">调试接口</span><span class="sxs-lookup"><span data-stu-id="4a8fc-136">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)