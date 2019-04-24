---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bf072aba27c90b7cea80c464e17fafb47524b695
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342087"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una matriz de las propiedades que utiliza un grupo de formularios.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parameters

 _pfrminfoarray_
  
> a Un puntero a una matriz de objetos de información de formulario que identifican los formularios para los que se devuelven propiedades.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se devuelve la matriz de propiedades en el parámetro _ppResults_ . Se pueden establecer los siguientes indicadores: 
    
FORMPROPSET_INTERSECTION 
  
> La matriz devuelta contiene la intersección de las propiedades del formulario.
    
FORMPROPSET_UNION 
  
> La matriz devuelta contiene la Unión de las propiedades del formulario.
    
MAPI_UNICODE 
  
> Las cadenas devueltas en la matriz tienen formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
 _ppResults_
  
> contempla Un puntero a un puntero a la estructura [SMAPIFormPropArray](smapiformproparray.md) devuelta, que contiene las propiedades que usan los formularios. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr:: CalcFormPropSet** para obtener una matriz de las propiedades que utiliza un grupo de formularios. <b0>CalcFormPropSet</b0> toma una intersección o una Unión de los conjuntos de propiedades de estos formularios, en función del indicador establecido en el parámetro <b1>ulFlags</b1> , y devuelve una estructura <b2>SMAPIFormPropArray</b2> que contiene el grupo resultante del </a1>. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si un visor de formularios pasa la marca MAPI_UNICODE en el parámetro _ulFlags_ , todas las cadenas deben devolverse como cadenas Unicode. Los proveedores de bibliotecas de formularios que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si se pasa MAPI_UNICODE. 
  
## <a name="see-also"></a>Vea también



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

