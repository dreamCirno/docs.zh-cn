---
description: '了解详细信息： Erase 语句 (Visual Basic) '
title: Erase 语句
ms.date: 07/20/2015
f1_keywords:
- vb.Erase
helpviewer_keywords:
- Erase keyword [Visual Basic]
- Erase statement [Visual Basic]
ms.assetid: 7a8133d7-b750-4d74-8b66-ba1dd9778d4b
ms.openlocfilehash: 295abec89f3d69f8f2641a5a3d574a2d10f98474
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99769151"
---
# <a name="erase-statement-visual-basic"></a>Erase 语句 (Visual Basic)

用于释放数组变量并解除分配用于其元素的内存。  
  
## <a name="syntax"></a>语法  
  
```vb  
Erase arraylist  
```  
  
## <a name="parts"></a>组成部分  

 `arraylist`  
 必需。 要清除的数组变量的列表。 以逗号分隔多个变量。  
  
## <a name="remarks"></a>备注  

 `Erase`语句只能出现在过程级别。 这意味着，可以在过程中释放数组，但不能在类或模块级别进行。  
  
 `Erase`语句等效于分配 `Nothing` 给每个数组变量。  
  
## <a name="example"></a>示例  

 下面的示例使用 `Erase` 语句来清除两个数组，并分别)  (1000 和100存储元素的内存。 `ReDim`然后，语句将新的数组实例赋给三维数组。  
  
 [!code-vb[VbVbalrStatements#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#19)]  
  
## <a name="see-also"></a>请参阅

- [Nothing](../nothing.md)
- [ReDim 语句](redim-statement.md)
