---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9c6a6d210230fc305aef46371c22f67b3d445a81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576585"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Devuelve una matriz de las propiedades de todos los formularios instalados en un contenedor de formulario.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se devuelve la matriz de propiedad en el parámetro _ppResults_ . Se pueden establecer los siguientes indicadores: 
    
FORMPROPSET_INTERSECTION 
  
> La matriz devuelta contiene la intersección de las propiedades de los formularios.
    
FORMPROPSET_UNION 
  
> La matriz devuelta contiene la unión de las propiedades de los formularios.
    
MAPI_UNICODE 
  
> Las cadenas devueltas en la matriz están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
 _ppResults_
  
> [out] Un puntero a un puntero a la estructura [SMAPIFormPropArray](smapiformproparray.md) devuelta. Esta estructura contiene todas las propiedades que se utilizan en los formularios instalados. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente de llaman al método **IMAPIFormContainer::CalcFormPropSet** para obtener una matriz de propiedades que se usan por todos los formularios instalados en un contenedor de formulario. **IMAPIFormContainer::CalcFormPropSet** funciona como el método [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) , salvo que opera en cada formulario registrado en un contenedor determinado. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Proveedores de biblioteca de formulario que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si se pasa MAPI_UNICODE..
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **IMAPIFormContainer::CalcFormPropSet** toma una intersección o una unión de conjuntos de propiedades de los formularios, dependiendo de la marca que se define en el parámetro _ulFlags_ , y devuelve una estructura **SMAPIFormPropArray** que contiene el grupo resultante de propiedades. 
  
Si un cliente pasa el indicador MAPI_UNICODE _ulFlags_, todas las cadenas devueltas son Unicode.
  
## <a name="see-also"></a>Vea también



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

