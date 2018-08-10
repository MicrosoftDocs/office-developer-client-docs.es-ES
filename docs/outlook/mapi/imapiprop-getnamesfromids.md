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
ms.openlocfilehash: a2ec6def319b1f4686a61e9f97a936bfeba0d410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817416"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**Hace referencia a**: Outlook 
  
Proporciona los nombres de propiedad que se corresponden con uno o varios identificadores de propiedad.
  
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
  
> [entrada, salida] En la entrada, un puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas (propiedad); de lo contrario, NULL, que indica que se deben devolver todos los nombres. El miembro **cValues** para la matriz de la etiqueta de propiedad no puede ser 0. Si _lppPropTags_ es un puntero válido en la entrada, **GetNamesFromIDs** devuelve los nombres de cada identificador de la propiedad incluidos en la matriz. 
    
 _lpPropSetGuid_
  
> [entrada] Un puntero a un GUID, [GUID](guid.md) o estructura, que identifica un conjunto de propiedades. El parámetro _lpPropSetGuid_ puede apuntar a un conjunto de propiedades válido o puede ser NULL. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de marcadores que indica el tipo de nombres que se va a devolver. Se pueden usar las siguientes marcas (si se establecen ambos marcadores, no hay nombres se devolverán):
    
MAPI_NO_IDS 
  
> Solicitudes que se va a devolver sólo los nombres almacenados como cadenas Unicode. 
    
MAPI_NO_STRINGS 
  
> Solicitudes que se va a devolver sólo los nombres almacenados como identificadores numéricos. 
    
 _lpcPropNames_
  
> [out] Un puntero a un recuento de los punteros de nombre de propiedad en la matriz indicada por el parámetro _lppPropNames_ . 
    
 _lpppPropNames_
  
> [out] Un puntero a una matriz de punteros a las estructuras [MAPINAMEID](mapinameid.md) que contiene los nombres de propiedad. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los nombres de propiedad correctamente se han devuelto. 
    
MAPI_E_NO_SUPPORT 
  
> El objeto no admite propiedades con nombre. 
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada satisfactoria, pero no se podrían devolver nombres para una o más propiedades. Las etiquetas de propiedad para las propiedades con errores tienen un tipo de propiedad de **PT_ERROR**. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md). 
    
MAPI_E_INVALID_PARAMETER 
  
> El miembro **cValues** de una o varias de las entradas de la matriz de etiqueta de propiedad que señala _lppPropTags_ se establece en 0. 
    
## <a name="remarks"></a>Comentarios

Mientras el acceso a la mayoría de las propiedades es por identificador de la propiedad, se pueden tener acceso a algunas propiedades por su nombre. El método **IMAPIProp::GetNamesFromIDs** se puede llamar para hacer lo siguiente: 
  
- Recuperar los nombres para los identificadores de propiedad concreta en un conjunto de propiedades específico.
    
- Recuperar los nombres para los identificadores de propiedad específico en cualquier conjunto de propiedades.
    
- Recuperar los nombres de todas las propiedades con nombre que se incluyen en la asignación del objeto.
    
Si configurar puntos de _lppPropTags_ a una matriz de etiqueta de la propiedad valid con uno o varios identificadores de propiedad y los puntos de _lpPropSetGuid_ a una propiedad válida, **GetNamesFromIDs** omite el conjunto de propiedades y los tipos de propiedad y devuelve todos los nombres de que se asignan a los identificadores de especificado. 
  
Si _lppPropTags_ puntos en una matriz de etiqueta de la propiedad valid con uno o varios identificadores de propiedad y _lpPropSetGuid_ es NULL, **GetNamesFromIDs** devuelve todos los nombres que se asignan a los identificadores de especificado. 
  
Si un identificador especificado no tiene un nombre, **GetNamesFromIDs** devuelve NULL en lugar de ese identificador en la estructura devuelta en _lpppPropNames_ y también devuelve MAPI_W_ERRORS_RETURNED. 
  
Si _lpPropSetGuid_ y _lppPropTags_ son NULL, **GetNamesFromIDs** asigna una nueva matriz de etiqueta de propiedad y devuelve todos los nombres de todas las propiedades con nombre para el objeto. 
  
Cuando no hay ningún nombre que se va a devolver, quizás porque no hay ninguna propiedad en el conjunto de propiedades solicitado o todas las propiedades son de un tipo excluido por los indicadores, **GetNamesFromIDs** hace lo siguiente: 
  
- Devuelve S_OK.
    
- Asigna una nueva estructura de **elemento SPropTagArray** , al establecer al miembro **cValues** en 0. 
    
- Establece el contenido de _lpcPropNames_ en 0. 
    
- El contenido de _lpppPropNames_ se establece en NULL. 
    
## <a name="notes-to-implementers"></a>Notas para los implementadores

Si los puntos de _lpPropSetGuid_ a un conjunto de propiedades válido y _lppPropTags_ es NULL, el resultado es indefinido. Puede usar una de las siguientes estrategias: 
  
- Omitir el conjunto de propiedades y devolver los nombres de los identificadores en la matriz de la etiqueta de propiedad.
    
- Devolver los nombres de los identificadores de sólo en la matriz de la etiqueta de propiedad que pertenecen al conjunto de propiedades especificado.
    
- Producirá un error en la llamada, devolución de MAPI_E_INVALID_PARAMETER. 
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar todas las propiedades de un objeto con nombre, debe llamar primero al método del objeto [IMAPIProp::GetPropList](imapiprop-getproplist.md) y, a continuación, pase los identificadores devueltos que están por encima del rango de 0 x 8000 a **GetNamesFromIDs**.
  
Si se pasan un conjunto de propiedades válido, pero no una matriz de la etiqueta de propiedad válido, esté preparado para resultados impredecibles. Algunas implementaciones de **GetNamesFromIDs** omitir el conjunto de propiedades y devuelven los nombres de los identificadores en la matriz de la etiqueta de propiedad. Algunas implementaciones devolver MAPI_E_INVALID_PARAMETER. Aún otras implementaciones de devuelven nombres para los identificadores de todas las propiedades en el conjunto de propiedades. Si el conjunto de propiedades es PS_PUBLIC_STRINGS, **GetNamesFromIDs** puede devolver todos los nombres que nunca se crearon. Si el proveedor de servicios almacena una propiedad en los identificadores de asociados con las cadenas públicas es irrelevante. 
  
Cuando haya terminado con los nombres de propiedad, compruebe el contenido del parámetro _lpcPropNames_ para determinar si los nombres se han devuelto. Si es así, llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria que señala _lppPropTags_ y _lpppPropNames_ cuando se devuelve un resultado correcto. Una llamada a **MAPIFreeBuffer** es suficiente para cada parámetro; no es necesario que recorrer la matriz de punteros y libre individualmente cada estructura **MAPINAMEID** . 
  
Para obtener más información acerca de las propiedades con nombre, vea [Propiedades de nombre de MAPI](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedProps  <br/> |MFCMAPI, utiliza el método **IMAPIProp::GetNamesFromIDs** para buscar propiedades con nombre que se han asignado anteriormente.  <br/> |
   
## <a name="see-also"></a>Vea también



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)
  
[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPINAMEID](mapinameid.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Con el nombre de las propiedades de MAPI](mapi-named-properties.md)
  
[Uso de macros para el control de errores](using-macros-for-error-handling.md)

