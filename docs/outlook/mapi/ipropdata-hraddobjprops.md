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
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416387"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega una o más propiedades de tipo PT Object al objeto.
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameters

 _lpPropTagArray_
  
> a Un puntero a una matriz de etiquetas de propiedad que indica las propiedades que se van a agregar.
    
 _lppProblems_
  
> [in, out] En la entrada, un puntero válido a una estructura [SPropProblemArray](spropproblemarray.md) o null. En la salida, un puntero a un puntero a una estructura que contiene información sobre las propiedades que no se han podido agregar o NULL. Un puntero a una propiedad se devuelve una estructura de matriz con problemas sólo si se pasa un puntero válido. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se agregaron correctamente.
    
MAPI_E_INVALID_TYPE 
  
> Se pasó un tipo de propiedad que no es PT Object en la matriz a la que apunta el parámetro _lpPropTagArray_ . 
    
MAPI_E_NO_ACCESS 
  
> El objeto se ha establecido para no permitir el permiso de lectura y escritura.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Se agregaron algunas de las propiedades, pero no todas.
    
## <a name="remarks"></a>Comentarios

El método **IPropData:: HrAddObjProps** agrega una o más propiedades de tipo PT Object al objeto. **HrAddObjProps** proporciona una alternativa al método [IMAPIProp:: SetProps](imapiprop-setprops.md) para propiedades de objeto, porque las propiedades de objeto no se pueden crear llamando a **SetProps**. Agregar una propiedad de objeto da como resultado la etiqueta Property que se va a incluir en la lista de etiquetas de propiedad que devuelve el método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si **HrAddObjProps** devuelve MAPI_W_PARTIAL_COMPLETION y ha establecido _lppProblems_ en un puntero válido, Compruebe la estructura de [SPropProblemArray](spropproblemarray.md) devuelta para averiguar qué propiedades no se han agregado. Normalmente, el único problema que se produce es la falta de memoria. Libere la estructura **SPropProblemArray** llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) cuando haya terminado con ella. 
  
Para agregar una propiedad, el objeto de destino debe tener permiso de lectura y escritura. Si **HrAddObjProps** devuelve MAPI_E_NO_ACCESS, no se pueden agregar propiedades al objeto porque no permite modificación. Para obtener permiso de lectura y escritura en un objeto antes de llamar a **HrAddObjProps**, llame a [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) y establezca el parámetro _ulAccess_ en IPROP_READWRITE. 
  
## <a name="see-also"></a>Ver también



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

