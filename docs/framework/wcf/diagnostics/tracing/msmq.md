---
description: 了解详细信息： MSMQ
title: MSMQ
ms.date: 03/30/2017
ms.assetid: d9fca29f-fa44-4ec4-bb48-b10800694500
ms.openlocfilehash: 3d694fdab202cd2b3b03c377f72d93c22cbae263
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99720574"
---
# <a name="msmq"></a>MSMQ

在 MSMQ 应用程序中，不会在 MSMQ 与队列通道之间传输任何额外活动。  
  
 另外，在执行 Send（发送）操作和 Receive（接收）操作时，还将 MSMQ 消息 ID 和 SOAP 消息 ID（连同活动 ID，如果存在）  
  
 作为队列通道跟踪的一部分来跟踪。  
  
 接收操作所需的传输的执行方式类似于任何其他传输 (接收字节->处理消息 > 操作) 。
