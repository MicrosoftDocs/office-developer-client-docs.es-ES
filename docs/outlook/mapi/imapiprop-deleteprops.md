---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 8eb19f9a2d3458e153b0758b56c502ce612be0cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817421"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**Se aplica a**: Outlook 
  
Elimina una o más propiedades de un objeto. 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Par�metros

 _lpPropTagArray_
  
> [entrada] Un puntero a una matriz de etiquetas de propiedad que indican las propiedades para eliminar. El miembro **cValues** de la estructura del [elemento SPropTagArray](sproptagarray.md) que señala _lpPropTagArray_ no debe ser cero, y el parámetro _lpPropTagArray_ propio no debe ser NULL. 
    
 _lppProblems_
  
> [entrada, salida] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no es necesario para obtener información de error. Si _lppProblems_ es un puntero válido en la entrada, **DeleteProps** devuelve información detallada acerca de los errores al eliminar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se eliminaron correctamente.
    
MAPI_E_NO_ACCESS 
  
> El autor de la llamada no tiene permisos suficientes para eliminar propiedades.
    
## <a name="remarks"></a>Notas

El método **IMAPIProp::DeleteProps** quita una o varias propiedades del objeto actual. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

No es necesario que permitir que las propiedades que se eliminará de todos los objetos. Si el objeto no es modificable, devuelva MAPI_E_NO_ACCESS desde el método **DeleteProps** . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No es necesario que establecer el tipo de propiedad para cada etiqueta de la propiedad en la matriz de etiqueta de la propiedad indicada por el parámetro _lpPropTagArray_ . Tipos de propiedad se omiten; se usan sólo los identificadores de propiedad. 
  
Tenga en cuenta que algunos objetos no permitir la modificación y que estos objetos devuelven MAPI_E_NO_ACCESS desde el método **DeleteProps** . Permitir que otros objetos de algunas propiedades que se va a eliminar, pero no para otros. Cuando hay un problema al eliminar sólo algunas de las propiedades, **DeleteProps** devuelve S_OK. Si han transcurrido un puntero válido en el parámetro _lppProblems_ , **DeleteProps** establecerá el puntero a una estructura **SPropProblemArray** que contiene información detallada acerca de los problemas con cada propiedad. Por ejemplo, si se va a eliminar todas las propiedades de un mensaje y hay un problema con uno o varios de sus datos adjuntos, la estructura **SPropProblemArray** contendrá una entrada para el **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)) (propiedad). 
  
La estructura que señala _lppProblems_ sólo es válida si **DeleteProps** devuelve S_OK. Si **DeleteProps** devuelve un error, no intente utilizar la estructura **SPropProblemArray** . En su lugar, llame al método del objeto [IMAPIProp::GetLastError](imapiprop-getlasterror.md) para obtener más información sobre el error. 
  
Libere la estructura **SPropProblemArray** devuelta mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI usa el método **IMAPIProp::DeleteProps** para eliminar una propiedad de un objeto.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[Elemento SPropTagArray](sproptagarray.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

