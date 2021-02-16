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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436429"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una matriz de las propiedades que usa un grupo de formularios.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parámetros

 _pfrminfoarray_
  
> [entrada] Puntero a una matriz de objetos de información de formulario que identifican los formularios para los que se devuelven propiedades.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se devuelve la matriz de propiedades en el parámetro _ppResults._ Se pueden establecer las siguientes marcas: 
    
FORMPROPSET_INTERSECTION 
  
> La matriz devuelta contiene la intersección de las propiedades del formulario.
    
FORMPROPSET_UNION 
  
> La matriz devuelta contiene la unión de las propiedades del formulario.
    
MAPI_UNICODE 
  
> Las cadenas devueltas en la matriz están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.
    
 _ppResults_
  
> [salida] Puntero a un puntero a la estructura [SMAPIFormPropArray](smapiformproparray.md) devuelta, que contiene las propiedades que usan los formularios. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr::CalcFormPropSet** para obtener una matriz de las propiedades que usa un grupo de formularios. **CalcFormPropSet** toma una intersección o una unión de los conjuntos de propiedades de estos formularios, según la marca establecida en el parámetro  _ulFlags,_ y devuelve una estructura **SMAPIFormPropArray** que contiene el grupo de propiedades resultante. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si un visor de formularios pasa MAPI_UNICODE marca en el parámetro  _ulFlags,_ todas las cadenas deben devolverse como cadenas Unicode. Los proveedores de bibliotecas de formularios que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE se pasa. 
  
## <a name="see-also"></a>Consulte también



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

