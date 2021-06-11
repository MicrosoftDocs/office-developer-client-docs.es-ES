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
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414917"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una matriz de las propiedades usadas por todos los formularios instalados en un contenedor de formularios.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se devuelve la matriz de propiedades en el _parámetro ppResults._ Se pueden establecer las siguientes marcas: 
    
FORMPROPSET_INTERSECTION 
  
> La matriz devuelta contiene la intersección de las propiedades de los formularios.
    
FORMPROPSET_UNION 
  
> La matriz devuelta contiene la unión de las propiedades de los formularios.
    
MAPI_UNICODE 
  
> Las cadenas devueltas en la matriz están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.
    
 _ppResults_
  
> [salida] Puntero a un puntero a la estructura [SMAPIFormPropArray](smapiformproparray.md) devuelta. Esta estructura contiene todas las propiedades usadas por los formularios instalados. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente llaman al método **IMAPIFormContainer::CalcFormPropSet** para obtener una matriz de propiedades usadas por todos los formularios instalados en un contenedor de formularios. **IMAPIFormContainer::CalcFormPropSet** funciona como el método [IMAPIFormMgr::CalcFormPropSet,](imapiformmgr-calcformpropset.md) excepto que funciona en todos los formularios registrados en un contenedor determinado. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Los proveedores de bibliotecas de formularios que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE se pasa.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **IMAPIFormContainer::CalcFormPropSet** toma una intersección o una unión de los conjuntos de propiedades de los formularios, según la marca establecida en el parámetro  _ulFlags,_ y devuelve una estructura **SMAPIFormPropArray** que contiene el grupo de propiedades resultante. 
  
Si un cliente pasa la marca MAPI_UNICODE en  _ulFlags_, todas las cadenas devueltas son Unicode.
  
## <a name="see-also"></a>Vea también



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

