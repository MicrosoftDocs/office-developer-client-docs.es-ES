---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412460"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera el valor de la propiedad de una o varias propiedades de un objeto.
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a>Parameters

 _lpPropTagArray_
  
> a Un puntero a una matriz de etiquetas de propiedad que identifican las propiedades cuyos valores se van a recuperar. El parámetro _lpPropTagArray_ debe ser null, que indica que deben devolverse los valores de todas las propiedades del objeto, o bien, apuntar a una estructura [SPropTagArray](sproptagarray.md) que contenga una o más etiquetas de propiedad. 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que indica el formato de las propiedades que tienen el tipo PT_UNSPECIFIED. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Los valores de cadena para estas propiedades deben devolverse en el formato Unicode. Si no se establece la marca MAPI_UNICODE, los valores de cadena deben devolverse en formato ANSI.
    
 _lpcValues_
  
> contempla Un puntero a un recuento de valores de propiedad apuntado por el parámetro _lppPropArray_ . Si _lppPropArray_ es null, el contenido del parámetro _lpcValues_ es cero. 
    
 _lppPropArray_
  
> contempla Un puntero a un puntero a los valores de propiedad recuperados.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los valores de la propiedad se recuperaron correctamente.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se realizó en general, pero no se pudo tener acceso a una o más propiedades. El miembro **aulPropTag** del valor de la propiedad para cada propiedad no disponible tiene un tipo de propiedad de PT_ERROR y un identificador de cero. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).
    
MAPI_E_INVALID_PARAMETER 
  
> Se pasó cero en el miembro **cValues** de la estructura **SPropTagArray** a la que apunta _lpPropTagArray_.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp:: GetProps** obtiene los valores de propiedad de una o varias propiedades de un objeto. 
  
Los valores de propiedad se devuelven en el mismo orden en que se solicitaron (es decir, el orden de propiedades en la matriz de etiquetas de propiedad a la que apunta _lpPropTagArray_ coincide con el orden de la matriz de estructuras de valores de propiedad apuntado por _lppPropArray _). 
  
Los tipos de propiedad especificados en los miembros **aulPropTag** de la matriz de etiquetas de propiedad indican el tipo de valor que se debe devolver en el miembro de **valor** de cada estructura de valor de propiedad. Sin embargo, si el autor de la llamada no conoce el tipo de una propiedad, el tipo del miembro **aulPropTag** se puede establecer en su lugar para PT_UNSPECIFIED. Al recuperar el valor, **GetProps** establece el tipo correcto en el miembro **aulPropTag** de la estructura del valor de la propiedad para la propiedad. 
  
Si los tipos de propiedad se especifican en **SPropTagArray** en _lpPropTagArray_, los valores de propiedad de **SPropValue** devueltos en _lppPropArray_ tienen tipos que coinciden exactamente con los tipos solicitados, a menos que se devuelva un valor de error. en lugar. 
  
Las propiedades de cadena pueden tener uno de los dos tipos de propiedades: PT_UNICODE para representar el formato Unicode y PT_STRING8 para representar el formato ANSI. Si la marca MAPI_UNICODE se establece en el parámetro _ulFlags_ , siempre que **GetProps** no pueda determinar el formato adecuado para una propiedad de cadena, devolverá su valor en formato Unicode. **GetProps** no puede determinar un tipo de propiedad de cadena exacta en las siguientes situaciones: 
  
- El parámetro _lpPropTagArray_ se establece en null para solicitar todas las propiedades. 
    
- El miembro **aulPropTag** incluye el valor PT_UNSPECIFIED como su tipo de propiedad en la matriz de etiquetas de propiedades. 
    
Si el parámetro _lpPropTagArray_ se establece en null para recuperar todas las propiedades del objeto y no existen propiedades, **GetProps** hace lo siguiente: 
  
- Devuelve S_OK.
    
- Establece en 0 el valor de recuento del miembro **cValues** de la estructura del valor de la propiedad. 
    
- Establece el contenido de _lpcValues_ en 0. 
    
- Establece _lppPropArray_ en NULL. 
    
 **GetProps** no debe devolver propiedades de varios valores con **cValues** establecido en 0. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Llame a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) para asignar memoria al principio para la estructura [SPropValue](spropvalue.md) a la que apunta _lpPropTagArray_; llamar a [MAPIAllocateMore](mapiallocatemore.md) para asignar la memoria adicional necesaria para los miembros de la estructura. 
  
Devuelve MAPI_W_ERRORS_RETURNED si no puede recuperar el valor de una o varias de las propiedades solicitadas. En la estructura del valor de la propiedad, establezca el tipo del miembro **aulPropTag** en PT_ERROR y el miembro **Value** en un código de estado que describe el error. Por ejemplo, si tiene que convertir una cadena en Unicode y no admite Unicode, establezca el **valor** de Member en MAPI_E_BAD_CHARWIDTH. Si la propiedad es demasiado grande, establézcalo en MAPI_E_NOT_ENOUGH_MEMORY. Si el objeto no admite la propiedad, establézcalo en MAPI_E_NOT_FOUND. 
  
La implementación de un proveedor de transporte remoto del método **GetProps** debe devolver los valores de propiedad de la carpeta para las propiedades solicitadas por el autor de la llamada. La implementación debe hacer lo siguiente: 
  
- Asigne una matriz de valores de propiedad para volver a la persona que llama y almacenar su dirección en el parámetro de puntero de valor de propiedad que se pasa para ese propósito.
    
- Copie las etiquetas de propiedad de las propiedades de la carpeta en las etiquetas de propiedad de la matriz de valores de propiedad de acuerdo con la matriz de etiquetas de propiedad pasadas a **GetProps**.
    
- Asegúrese de que el tipo de propiedad está establecido para todas las etiquetas de propiedad pasadas a **GetProps**. El autor de la llamada puede pasar un tipo de propiedad de PT_UNSPECIFIED, en cuyo caso **GetProps** debe establecer el tipo de propiedad correcto para esa etiqueta de propiedad. 
    
- Establezca el valor de cada propiedad en la matriz de valores de propiedad según su etiqueta. Por ejemplo, si la etiqueta de propiedad solicitada por el autor de la llamada es **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** puede establecer el valor en MAPI_FOLDER. 
    
- Si el autor de la llamada pasa cualquier etiqueta de propiedad que su implementación no controla, puede establecer la etiqueta de propiedad en PT_ERROR para esas propiedades y establecer el valor de la propiedad en MAPI_E_NOT_FOUND.
    
- Devuelve S_OK si no se han producido errores o MAPI_W_ERRORS_RETURNED si hay errores.
    
La implementación de un proveedor de transporte remoto del método **GetProps** debe admitir las siguientes propiedades como mínimo: 
  
- **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))
    
- **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))
    
- **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_OBJECT_TYPE**
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Para propiedades de tipo PT Object, llame al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) en lugar de a **GetProps**. 
  
Para las propiedades seguras, no espere recuperarlas llamando a **GetProps** con el parámetro _LPPPROPTAGARRAY_ establecido en NULL. Debe establecer explícitamente un identificador de propiedad segura en el miembro **aulPropTag** de su matriz de etiquetas de propiedad cuando llame a **GetProps**. Cuándo y cómo una propiedad segura está disponible en el proveedor de servicios. 
  
Libere la estructura **SPropValue** devuelta llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) solo si **GetProps** Devuelve S_OK o MAPI_W_ERRORS_RETURNED. 
  
Si **GetProps** devuelve MAPI_W_ERRORS_RETURNED porque no pudo obtener acceso a una o más propiedades, compruebe las etiquetas de propiedad de las propiedades devueltas. Las propiedades con error tendrán los siguientes valores establecidos en su estructura de valores de propiedad: 
  
- El tipo de propiedad en el miembro **aulPropTag** se establece en PT_ERROR. 
    
- El valor de la propiedad en el **valor** miembro establecido en un código de estado para el error, como MAPI_E_NOT_FOUND. 
    
Propiedades que dan error porque son demasiado grandes como para que se devuelvan convenientemente en la estructura del valor de la propiedad, establezca el valor del miembro **Value** en MAPI_E_NOT_ENOUGH_MEMORY. Normalmente, esto ocurre con las propiedades String o Binary de tipo PT_STRING8, PT_UNICODE o PT_BINARY cuando el valor de la propiedad es 4 KB o superior. Llamar a **IMAPIProp:: OpenProperty** para recuperar propiedades grandes. 
  
No todas las implementaciones de **GetProps** admiten los formatos Unicode y ANSI para las cadenas de caracteres. Cuando una propiedad determinada requiere la conversión de formato de cadena y **GetProps** no la admite, el valor del miembro **Value** de la propiedad se establece en MAPI_E_BAD_CHARWIDTH. 
  
Para comprobar si un PST es un archivo PST de SharePoint, Monte el archivo PST con [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md)y, a continuación, llame a **GetProps** en el objeto de almacén de mensajes que solicita esta propiedad. Si existe, puede suponer que el archivo PST se ha configurado para SharePoint; de lo contrario, el archivo PST no se ha configurado como un archivo PST de SharePoint. 
  
Para obtener más información acerca de cómo usar **GetProps** para obtener acceso a las propiedades, vea [recuperar propiedades de MAPI](retrieving-mapi-properties.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI usa el método **IMAPIProp:: GetProps** para obtener todas las propiedades de un objeto pasando un valor null o la matriz devuelta por el método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) en el parámetro _lpPropTagArray_ .  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Recuperación de propiedades MAPI](retrieving-mapi-properties.md)
  
[Uso de macros para el control de errores](using-macros-for-error-handling.md)

