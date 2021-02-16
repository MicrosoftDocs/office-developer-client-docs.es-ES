---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f6688afde9b36a7722eaaf768f091481c15b7308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423576"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona los nombres de propiedad que corresponden a uno o más identificadores de propiedad.
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a>Parámetros

 _lppPropTags_
  
> [entrada, salida] En la entrada, un puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad; de lo contrario, NULL, que indica que se deben devolver todos los nombres. El **miembro cValues** de la matriz de etiquetas de propiedades no puede ser 0. Si  _lppPropTags es_ un puntero válido en la entrada, **GetNamesFromIDs** devuelve nombres para cada identificador de propiedad incluido en la matriz. 
    
 _lpPropSetGuid_
  
> [entrada] Puntero a un GUID o estructura [GUID](guid.md) que identifica un conjunto de propiedades. El  _parámetro lpPropSetGuid_ puede apuntar a un conjunto de propiedades válido o puede ser NULL. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que indica el tipo de nombres que se devolverán. Se pueden usar las siguientes marcas (si se establecen ambas marcas, no se devolverá ningún nombre):
    
MAPI_NO_IDS 
  
> Solicita que solo se devuelvan los nombres almacenados como cadenas Unicode. 
    
MAPI_NO_STRINGS 
  
> Solicita que solo se devuelvan los nombres almacenados como identificadores numéricos. 
    
 _lpcPropNames_
  
> [salida] Puntero a un recuento de punteros de nombre de propiedad en la matriz a la que apunta el parámetro _lppPropNames._ 
    
 _lpppPropNames_
  
> [salida] Puntero a una matriz de punteros a estructuras [MAPINAMEID](mapinameid.md) que contienen nombres de propiedad. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los nombres de las propiedades se devolvieron correctamente. 
    
MAPI_E_NO_SUPPORT 
  
> El objeto no admite propiedades con nombre. 
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se ha hecho correctamente en general, pero no se pudieron devolver los nombres de una o más propiedades. Las etiquetas de propiedad de las propiedades con error tienen un tipo de propiedad **de PT_ERROR**. Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta. Para probar esta advertencia, use la **macro HR_FAILED** datos. Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md) 
    
MAPI_E_INVALID_PARAMETER 
  
> El **miembro cValues** de una o varias de las entradas de la matriz de etiquetas de propiedades a las que  _apunta lppPropTags_ se establece en 0. 
    
## <a name="remarks"></a>Comentarios

Aunque el acceso a la mayoría de las propiedades es por identificador de propiedad, se puede tener acceso a algunas propiedades por nombre. Se puede llamar al método **IMAPIProp::GetNamesFromIDs** para hacer lo siguiente: 
  
- Recuperar nombres de identificadores de propiedad específicos en un conjunto de propiedades específico.
    
- Recuperar nombres para identificadores de propiedad específicos en cualquier conjunto de propiedades.
    
- Recupere los nombres de todas las propiedades con nombre que se incluyen en la asignación del objeto.
    
Si  _lppPropTags_ apunta a una matriz de etiquetas de propiedad válida con uno o más identificadores de propiedad y  _lpPropSetGuid_ apunta a un conjunto de propiedades válido, **GetNamesFromIDs** omite el conjunto de propiedades y los tipos de propiedad y devuelve todos los nombres que se asignan a los identificadores especificados. 
  
Si  _lppPropTags_ apunta a una matriz de etiquetas de propiedad válida con uno o más identificadores de propiedad y  _lpPropSetGuid_ es NULL, **GetNamesFromIDs** devuelve todos los nombres que se asignan a los identificadores especificados. 
  
Si un identificador especificado no tiene un nombre, **GetNamesFromIDs** devuelve NULL en el lugar de ese identificador en la estructura devuelta en  _lpppPropNames_ y también devuelve MAPI_W_ERRORS_RETURNED. 
  
Si  _tanto lpPropSetGuid_ como  _lppPropTags_ son NULL, **GetNamesFromIDs** asigna una nueva matriz de etiquetas de propiedad y devuelve todos los nombres de todas las propiedades con nombre para el objeto. 
  
Cuando no hay nombres que devolver, quizás porque no hay propiedades en el conjunto de propiedades solicitadas o todas las propiedades son de un tipo excluido por las marcas, **GetNamesFromIDs** hace lo siguiente: 
  
- Devuelve S_OK.
    
- Asigna una nueva **estructura SPropTagArray,** estableciendo el **miembro cValues** en 0. 
    
- Establece el contenido  _de lpcPropNames_ en 0. 
    
- Establece el contenido de  _lpppPropNames_ en NULL. 
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si  _lpPropSetGuid_ apunta a un conjunto de propiedades válido y  _lppPropTags_ es NULL, el resultado es indefinido. Puede usar una de las siguientes estrategias: 
  
- Ignore el conjunto de propiedades y devuelva los nombres de los identificadores de la matriz de etiquetas de propiedad.
    
- Devuelve los nombres de solo los identificadores de la matriz de etiquetas de propiedades que pertenecen al conjunto de propiedades especificado.
    
- Se producirá un error en la llamada, MAPI_E_INVALID_PARAMETER. 
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar todas las propiedades con nombre de un objeto, primero debe llamar al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) del objeto y, a continuación, pasar los identificadores devueltos que están por encima del intervalo 0x8000 a **GetNamesFromIDs**.
  
Si pasa un conjunto de propiedades válido pero no una matriz de etiquetas de propiedad válida, esté preparado para obtener resultados impredecibles. Algunas implementaciones de **GetNamesFromIDs** omiten el conjunto de propiedades y devuelven los nombres de los identificadores de la matriz de etiquetas de propiedad. Algunas implementaciones devuelven MAPI_E_INVALID_PARAMETER. Aún así, otras implementaciones devuelven nombres para identificadores de todas las propiedades del conjunto de propiedades. Si el conjunto de propiedades PS_PUBLIC_STRINGS, **GetNamesFromIDs** puede devolver todos los nombres que se crearon. No importa si el proveedor de servicios almacena una propiedad en los identificadores asociados con las cadenas públicas. 
  
Cuando haya terminado con los nombres de propiedad, compruebe el contenido del parámetro  _lpcPropNames_ para determinar si se han devuelto nombres. Si es así, llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria a la que  _apuntan lppPropTags_ y  _lpppPropNames_ cuando se devuelve un resultado correcto. Una llamada a **MAPIFreeBuffer** es suficiente para cada parámetro; No es necesario recorrer la matriz de punteros y liberar individualmente cada **estructura MAPINAMEID.** 
  
Para obtener más información acerca de las propiedades con nombre, vea [propiedades con nombre MAPI](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedProps  <br/> |MFCMAPI usa el **método IMAPIProp::GetNamesFromIDs** para buscar propiedades con nombre que se han asignado anteriormente.  <br/> |
   
## <a name="see-also"></a>Consulte también



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)
  
[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPINAMEID](mapinameid.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Propiedades con nombre MAPI](mapi-named-properties.md)
  
[Uso de macros para el control de errores](using-macros-for-error-handling.md)

