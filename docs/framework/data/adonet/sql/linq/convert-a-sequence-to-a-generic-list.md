---
description: 了解详细信息：将序列转换为泛型列表
title: 将某一序列转换为泛型列表
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7ab76d93-6898-4e75-b76f-290a66ecead8
ms.openlocfilehash: e9832fd366f22b77674fb4c83f6af7ce89a552c5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99663113"
---
# <a name="convert-a-sequence-to-a-generic-list"></a>将某一序列转换为泛型列表

使用 <xref:System.Linq.Enumerable.ToList%2A> 可从序列创建泛型列表。  
  
## <a name="example"></a>示例  

 下面的示例使用 <xref:System.Linq.Enumerable.ToList%2A> 直接将查询的计算结果放入泛型 <xref:System.Collections.Generic.List%601>。  
  
 [!code-csharp[DLinqQueryExamples#45](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#45)]
 [!code-vb[DLinqQueryExamples#45](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#45)]  
  
## <a name="see-also"></a>请参阅

- [查询示例](query-examples.md)
