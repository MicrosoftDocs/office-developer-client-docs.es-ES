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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a0d86b9b0342beea6b33db0219cb5889d2e63f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592076"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp::DeleteProps** quita una o varias propiedades del objeto actual. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

No es necesario que permitir que las propiedades que se eliminará de todos los objetos. Si el objeto no es modificable, devuelva MAPI_E_NO_ACCESS desde el método **DeleteProps** . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No es necesario que establecer el tipo de propiedad para cada etiqueta de la propiedad en la matriz de etiqueta de la propiedad indicada por el parámetro _lpPropTagArray_ . Tipos de propiedad se omiten; se usan sólo los identificadores de propiedad. 
  
Tenga en cuenta que algunos objetos no permitir la modificación y que estos objetos devuelven MAPI_E_NO_ACCESS desde el método **DeleteProps** . Permitir que otros objetos de algunas propiedades que se va a eliminar, pero no para otros. Cuando hay un problema al eliminar sólo algunas de las propiedades, **DeleteProps** devuelve S_OK. Si han transcurrido un puntero válido en el parámetro _lppProblems_ , **DeleteProps** establecerá el puntero a una estructura **SPropProblemArray** que contiene información detallada acerca de los problemas con cada propiedad. Por ejemplo, si se va a eliminar todas las propiedades de un mensaje y hay un problema con uno o varios de sus datos adjuntos, la estructura **SPropProblemArray** contendrá una entrada para el **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)) (propiedad). 
  
La estructura que señala _lppProblems_ sólo es válida si **DeleteProps** devuelve S_OK. Si **DeleteProps** devuelve un error, no intente utilizar la estructura **SPropProblemArray** . En su lugar, llame al método del objeto [IMAPIProp::GetLastError](imapiprop-getlasterror.md) para obtener más información sobre el error. 
  
Libere la estructura **SPropProblemArray** devuelta mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI usa el método **IMAPIProp::DeleteProps** para eliminar una propiedad de un objeto.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

