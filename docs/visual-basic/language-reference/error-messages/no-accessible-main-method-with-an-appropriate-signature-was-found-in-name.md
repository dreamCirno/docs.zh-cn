---
description: 了解详细信息： BC30737：在 "" 中找不到带有适当签名的可访问 "Main" 方法 <name>
title: 在“<name>”中找不到任何具有合适签名的可访问“Main”方法
ms.date: 07/20/2015
f1_keywords:
- bc30737
- vbc30737
helpviewer_keywords:
- BC30737
ms.assetid: 3f40bacd-3fac-4741-b204-852f693d4340
ms.openlocfilehash: 5ff79c1b7589f6b67492ad640179f7a852a2f381
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100483516"
---
# <a name="bc30737-no-accessible-main-method-with-an-appropriate-signature-was-found-in-name"></a>BC30737：在 "" 中找不到带有适当签名的可访问 "Main" 方法 \<name>

命令行应用程序必须具有 `Sub Main` 定义的。 `Main` 必须声明为 `Public Shared` ，如同它是在类中定义的一样，或与 `Public` 在模块中定义的一样。

 **错误 ID：** BC30737

## <a name="to-correct-this-error"></a>更正此错误

- 定义 `Public Sub Main` 项目的过程。 当 `Shared` 且仅当在类中定义时，才将其声明为。

## <a name="see-also"></a>请参阅

- [Visual Basic 程序的结构](../../programming-guide/program-structure/structure-of-a-visual-basic-program.md)
- [过程](../../programming-guide/language-features/procedures/index.md)
