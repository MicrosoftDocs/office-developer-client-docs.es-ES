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
ms.openlocfilehash: 5bfef87baa2dffa4605f9a7afa3833024f514430
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409240"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Elimina una o más propiedades de un objeto. 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parámetros

 _lpPropTagArray_
  
> [entrada] Puntero a una matriz de etiquetas de propiedad que indican las propiedades que se eliminarán. El **miembro cValues** de la estructura [SPropTagArray](sproptagarray.md) a la que apunta  _lpPropTagArray_ no debe ser cero y el propio parámetro  _lpPropTagArray_ no debe ser NULL. 
    
 _lppProblems_
  
> [entrada, salida] En la entrada, un puntero a un puntero a una [estructura SPropProblemArray;](spropproblemarray.md) de lo contrario, NULL, que indica que no es necesario obtener información de errores. Si  _lppProblems_ es un puntero válido en la entrada, **DeleteProps** devuelve información detallada sobre los errores al eliminar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se eliminaron correctamente.
    
MAPI_E_NO_ACCESS 
  
> El llamador no tiene permisos suficientes para eliminar propiedades.
    
## <a name="remarks"></a>Comentarios

El **método IMAPIProp::D eleteProps** quita una o más propiedades del objeto actual. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

No es necesario permitir que las propiedades se eliminen de todos los objetos. Si el objeto no es modificable, devuelva MAPI_E_NO_ACCESS del **método DeleteProps.** 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No es necesario establecer el tipo de propiedad para cada etiqueta de propiedad en la matriz de etiquetas de propiedad a la que apunta el parámetro _lpPropTagArray._ Los tipos de propiedad se omiten; solo se usan los identificadores de propiedad. 
  
Tenga en cuenta que algunos objetos no permiten la modificación y que estos objetos devuelven MAPI_E_NO_ACCESS del **método DeleteProps.** Otros objetos permiten que algunas propiedades se eliminen, pero no otras. Cuando se produce un problema al eliminar solo algunas de las propiedades, **DeleteProps** devuelve S_OK. Si ha pasado un puntero válido en el parámetro  _lppProblems,_ **DeleteProps** establecerá el puntero en una estructura **SPropProblemArray** que contiene información detallada sobre los problemas con cada propiedad. Por ejemplo, si elimina todas las propiedades de un mensaje y hay un problema con uno o varios de sus datos adjuntos, la estructura **SPropProblemArray** contendrá una entrada para la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
La estructura a la que  _apunta lppProblems_ solo es válida si **DeleteProps** devuelve S_OK. Si **DeleteProps devuelve** un error, no intente usar la **estructura SPropProblemArray.** En su lugar, llame al método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) del objeto para obtener más información sobre el error. 
  
Libera la estructura **SPropProblemArray** devuelta llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI usa el **método IMAPIProp::D eleteProps** para eliminar una propiedad de un objeto.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

