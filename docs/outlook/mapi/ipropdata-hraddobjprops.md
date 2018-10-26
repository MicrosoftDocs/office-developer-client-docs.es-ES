---
title: IPropDataHrAddObjProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ae0d6d58f96738a9686dbdda86336c040c2e2f68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591693"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Agrega una o más propiedades de tipo pt Object para el objeto.
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Par�metros

 _lpPropTagArray_
  
> [entrada] Un puntero a una matriz de etiquetas de propiedad que indican las propiedades para agregar.
    
 _lppProblems_
  
> [entrada, salida] En la entrada, un puntero a una estructura [SPropProblemArray](spropproblemarray.md) , válido o NULL. En resultado, un puntero a un puntero a una estructura que contiene información acerca de las propiedades que no se pudo agregar o NULL. Se devuelve un puntero a una estructura de matriz de propiedad problema sólo si se pasa un puntero válido en. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se han agregado correctamente.
    
MAPI_E_INVALID_TYPE 
  
> Una propiedad de tipo que se pasó pt Object en la matriz que señala el parámetro _lpPropTagArray_ . 
    
MAPI_E_NO_ACCESS 
  
> El objeto se estableció para no permitir el permiso de lectura y escritura.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Algunos, pero no todos, de las propiedades que se han agregado.
    
## <a name="remarks"></a>Comentarios

El método **IPropData::HrAddObjProps** agrega una o más propiedades de tipo pt Object para el objeto. **HrAddObjProps** proporciona una alternativa al método [IMAPIProp::SetProps](imapiprop-setprops.md) para las propiedades del objeto, debido a que las propiedades del objeto no se puede crear llamando **SetProps**. Adición de resultado de una propiedad de objeto en la etiqueta de propiedad que se encuentran en la lista de etiquetas de propiedad que devuelve el método [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si **HrAddObjProps** devuelve MAPI_W_PARTIAL_COMPLETION y ha establecido _lppProblems_ a un puntero válido, compruebe la estructura [SPropProblemArray](spropproblemarray.md) devuelta para averiguar qué propiedades no se han agregado. Normalmente, el único problema que se produce es la falta de memoria. Libere la estructura **SPropProblemArray** mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) cuando haya terminado con él. 
  
Para agregar una propiedad, el objeto de destino debe tener permiso de lectura y escritura. Si **HrAddObjProps** devuelve MAPI_E_NO_ACCESS, no se puede agregar propiedades al objeto debido a que no permite la modificación. Para obtener permiso de lectura y escritura a un objeto antes de llamar a **HrAddObjProps**, llame [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) y establezca el parámetro _ulAccess_ en IPROP_READWRITE. 
  
## <a name="see-also"></a>Vea también



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

