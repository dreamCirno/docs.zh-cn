---
description: 了解详细信息： ICLROnEventManager 接口
title: ICLROnEventManager 接口
ms.date: 03/30/2017
api_name:
- ICLROnEventManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLROnEventManager
helpviewer_keywords:
- ICLROnEventManager interface [.NET Framework hosting]
ms.assetid: 9e15a0c1-8ab6-43d0-ae28-6ec7a4edd913
topic_type:
- apiref
ms.openlocfilehash: 7a9c0beec5083bc93f5361bb0e701da5beeedea2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789822"
---
# <a name="iclroneventmanager-interface"></a>ICLROnEventManager 接口

提供一些方法，这些方法允许主机注册和注销公共语言运行时 (CLR) 事件的回调。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[RegisterActionOnEvent 方法](iclroneventmanager-registeractiononevent-method.md)|为指定事件注册回调指针。|  
|[UnregisterActionOnEvent 方法](iclroneventmanager-unregisteractiononevent-method.md)|为指定的事件注销先前注册的回调指针。|  
  
## <a name="remarks"></a>备注  

 若要注册和注销事件回调，主机可 `ICLROnEventManager` 通过调用 [ICLRControl：： GetCLRManager](iclrcontrol-getclrmanager-method.md) 方法获取对的引用。  
  
> [!NOTE]
> [EClrEvent](eclrevent-enumeration.md)描述的事件可以从不同的线程激发一次，以指示卸载或禁用 CLR。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [EClrEvent 枚举](eclrevent-enumeration.md)
- [IActionOnCLREvent 接口](iactiononclrevent-interface.md)
- [ICLRControl 接口](iclrcontrol-interface.md)
- [承载接口](hosting-interfaces.md)
