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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: abd2a3e2a1a810f902ad977413c89f2e8b0113a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817293"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**Se aplica a**: Outlook 
  
Devuelve una matriz de las propiedades que utiliza un grupo de formularios.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Sintaxis

 _pfrminfoarray_
  
> [entrada] Un puntero a una matriz de objetos de información de formulario que identifican los formularios que se va a devolver propiedades.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se devuelve la matriz de propiedad en el parámetro _ppResults_ . Se pueden establecer los siguientes indicadores: 
    
FORMPROPSET_INTERSECTION 
  
> La matriz devuelta contiene la intersección de las propiedades del formulario.
    
FORMPROPSET_UNION 
  
> La matriz devuelta contiene la unión de las propiedades del formulario.
    
MAPI_UNICODE. 
  
> Las cadenas devueltas en la matriz están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
 _ppResults_
  
> [out] Un puntero a un puntero a la estructura [SMAPIFormPropArray](smapiformproparray.md) devuelta, que contiene las propiedades que usan los formularios. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.
    
## <a name="remarks"></a>Notas

Visores de formulario llamar al método **IMAPIFormMgr::CalcFormPropSet** para obtener una matriz de las propiedades que utiliza un grupo de formularios. **CalcFormPropSet** toma puede ser una intersección o una unión de propiedad estos formularios establece, según el indicador establecido en el parámetro _ulFlags_ y se devuelve una estructura **SMAPIFormPropArray** que contiene el grupo resultante de Propiedades. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Si un visor de formulario, pasa el indicador MAPI_UNICODE el parámetro _ulFlags_ , se deberían devolver todas las cadenas como cadenas Unicode. Proveedores de biblioteca de formulario que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si se pasa MAPI_UNICODE.. 
  
## <a name="see-also"></a>Ver también



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)

