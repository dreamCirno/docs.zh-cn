---
description: 了解详细信息： IMetaDataEmit：:D efineParam 方法
title: IMetaDataEmit::DefineParam 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineParam
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineParam
helpviewer_keywords:
- IMetaDataEmit::DefineParam method [.NET Framework metadata]
- DefineParam method [.NET Framework metadata]
ms.assetid: d86a3d14-4796-4909-9591-dfafe3de5ce4
topic_type:
- apiref
ms.openlocfilehash: 300de3183b329773a8e6813d6b92c6d049d63195
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784088"
---
# <a name="imetadataemitdefineparam-method"></a>IMetaDataEmit::DefineParam 方法

创建具有指定标记所引用的方法的指定签名的参数定义，并获取该参数定义的标记。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT DefineParam (  
    [in]  mdMethodDef md,
    [in]  ULONG       ulParamSeq,
    [in]  LPCWSTR     szName,
    [in]  DWORD       dwParamFlags,
    [in]  DWORD       dwCPlusTypeFlag,
    [in]  void const  *pValue,  
    [in]  ULONG       cchValue,
    [out] mdParamDef  *ppd
);  
```  
  
## <a name="parameters"></a>参数  

 `md`  
 中正在定义其参数的方法的标记。  
  
 `ulParamSeq`  
 中参数序列号。  
  
 `szName`  
 中Unicode 中参数的名称。  
  
 `dwParamFlags`  
 中参数的标志。 这是一个值的位掩码 `CorParamAttr` 。  
  
 `dwCPlusTypeFlag`  
 [in] `ELEMENT_TYPE_` *\** 用于常量值。  
  
 `pValue`  
 中参数的常数值。  
  
 `cchValue`  
 中的大小（以 Unicode 字符为格式） `pValue` 。  
  
 `ppd`  
 弄 `mdParamDef` 分配的令牌。  
  
## <a name="remarks"></a>备注  

 参数的序列值 `ulParamSeq` 从1开始。 返回值的序列号为0。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MSCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataEmit 接口](imetadataemit-interface.md)
- [IMetaDataEmit2 接口](imetadataemit2-interface.md)
