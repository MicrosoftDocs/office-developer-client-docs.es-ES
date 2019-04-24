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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329066"
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

## <a name="parameters"></a>Parameters

 _lppPropTags_
  
> [in, out] En la entrada, un puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad; de lo contrario, NULL, que indica que deben devolverse todos los nombres. El miembro **cValues** de la matriz de etiquetas de propiedades no puede ser 0. Si _lppPropTags_ es un puntero válido en la entrada, **GetNamesFromIDs** devuelve los nombres de todos los identificadores de propiedad incluidos en la matriz. 
    
 _lpPropSetGuid_
  
> a Un puntero a un GUID, o estructura [GUID](guid.md) , que identifica un conjunto de propiedades. El parámetro _lpPropSetGuid_ puede apuntar a un conjunto de propiedades válido o puede ser null. 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que indica el tipo de nombres que se va a devolver. Se pueden usar los siguientes indicadores (si se establecen ambos indicadores, no se devolverán nombres):
    
MAPI_NO_IDS 
  
> Se devuelven las solicitudes que solo tienen nombres almacenados como cadenas Unicode. 
    
MAPI_NO_STRINGS 
  
> Se devuelven las solicitudes que solo tienen nombres almacenados como identificadores numéricos. 
    
 _lpcPropNames_
  
> contempla Un puntero a un recuento de los punteros de nombre de propiedad en la matriz señalada por el parámetro _lppPropNames_ . 
    
 _lpppPropNames_
  
> contempla Un puntero a una matriz de punteros a estructuras [MAPINAMEID](mapinameid.md) que contiene los nombres de las propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los nombres de las propiedades se devolvieron correctamente. 
    
MAPI_E_NO_SUPPORT 
  
> El objeto no admite propiedades con nombre. 
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se realizó en general, pero no se pudieron devolver los nombres de una o más propiedades. Las etiquetas de propiedad de las propiedades con error tienen un tipo de propiedad de **PT_ERROR**. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md). 
    
MAPI_E_INVALID_PARAMETER 
  
> El miembro **cValues** de una o varias entradas de la matriz de etiquetas de propiedad a la que señala _lppPropTags_ se establece en 0. 
    
## <a name="remarks"></a>Comentarios

Mientras que el acceso a la mayoría de las propiedades es por identificador de propiedad, se puede tener acceso a algunas propiedades por nombre. Se puede llamar al método **IMAPIProp:: GetNamesFromIDs** para hacer lo siguiente: 
  
- Recuperar nombres de identificadores de propiedad específicos en un conjunto de propiedades específico.
    
- Recuperar nombres de identificadores de propiedad específicos en cualquier conjunto de propiedades.
    
- Recuperar los nombres de todas las propiedades con nombre que se incluyen en la asignación del objeto.
    
Si _lppPropTags_ apunta a una matriz de etiquetas de propiedad válida con uno o más identificadores de propiedad y _lpPropSetGuid_ apunta a un conjunto de propiedades válido, **GetNamesFromIDs** omite el conjunto de propiedades y los tipos de propiedad y devuelve todos los nombres. que se asignan a los identificadores especificados. 
  
Si _lppPropTags_ apunta a una matriz de etiquetas de propiedad válida con uno o más identificadores de propiedad y _lpPropSetGuid_ es null, **GetNamesFromIDs** devuelve todos los nombres que se asignan a los identificadores especificados. 
  
Si un identificador especificado no tiene un nombre, **GetNamesFromIDs** devuelve null en el lugar de ese identificador en la estructura devuelta en _lpppPropNames_ y también devuelve MAPI_W_ERRORS_RETURNED. 
  
Si tanto _lpPropSetGuid_ como _lppPropTags_ son NULL, **GetNamesFromIDs** asigna una nueva matriz de etiquetas de propiedad y devuelve todos los nombres de todas las propiedades con nombre del objeto. 
  
Cuando no hay ningún nombre que devolver, quizá porque no hay propiedades en el conjunto de propiedades solicitadas o todas las propiedades son de un tipo excluido por los marcadores, **GetNamesFromIDs** hace lo siguiente: 
  
- Devuelve S_OK.
    
- Asigna una nueva estructura **SPropTagArray** , estableciendo el miembro **cValues** en 0. 
    
- Establece el contenido de _lpcPropNames_ en 0. 
    
- Establece el contenido de _lpppPropNames_ en NULL. 
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si _lpPropSetGuid_ apunta a un conjunto de propiedades válido y _lppPropTags_ es null, el resultado es undefined. Puede usar una de las siguientes estrategias: 
  
- Omitir el conjunto de propiedades y devolver los nombres de los identificadores en la matriz de etiquetas de propiedades.
    
- Devolver los nombres de solo los identificadores de la matriz de etiquetas de propiedades que pertenecen al conjunto de propiedades especificado.
    
- Suspenda la llamada, devolviendo MAPI_E_INVALID_PARAMETER. 
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar todas las propiedades con nombre de un objeto, primero debe llamar al método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) del objeto y, a continuación, pasar los identificadores devueltos que están por encima del intervalo 0X8000 a **GetNamesFromIDs**.
  
Si pasa un conjunto de propiedades válido, pero no una matriz de etiquetas de propiedad válida, prepárese para los resultados impredecibles. Algunas implementaciones de **GetNamesFromIDs** ignoran el conjunto de propiedades y devuelven los nombres de los identificadores en la matriz de etiquetas de propiedades. Algunas implementaciones devuelven MAPI_E_INVALID_PARAMETER. Todavía otras implementaciones devuelven los nombres de los identificadores de todas las propiedades del conjunto de propiedades. Si el conjunto de propiedades es PS_PUBLIC_STRINGS, **GetNamesFromIDs** puede devolver todos los nombres que se hayan creado en algún momento. El hecho de que el proveedor de servicios almacene una propiedad en los identificadores asociados a las cadenas públicas es irrelevante. 
  
Cuando haya terminado con los nombres de propiedad, compruebe el contenido del parámetro _lpcPropNames_ para determinar si se han devuelto nombres. Si es así, llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria a la que apunta _lppPropTags_ y _lpppPropNames_ cuando se devuelve un resultado correcto. Una llamada a **MAPIFreeBuffer** es suficiente para cada parámetro; no es necesario atravesar la matriz de punteros y liberar cada estructura **MAPINAMEID** de forma individual. 
  
Para obtener más información acerca de las propiedades con nombre, consulte [MAPI con nombre de propiedades](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl. cpp  <br/> |CSingleMAPIPropListCtrl:: FindAllNamedProps  <br/> |MFCMAPI usa el método **IMAPIProp:: GetNamesFromIDs** para buscar propiedades con nombre que se han asignado anteriormente.  <br/> |
   
## <a name="see-also"></a>Vea también



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

