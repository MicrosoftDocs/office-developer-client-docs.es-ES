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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 33351235db2a9a3f9d9b67f59e8356a0fa8abfa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817410"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**Se aplica a**: Outlook 
  
Recupera el valor de la propiedad de una o varias propiedades de un objeto.
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a>Par�metros

 _lpPropTagArray_
  
> [entrada] Un puntero a una matriz de etiquetas (propiedad) que identifican las propiedades cuyos valores se van a recuperar. El parámetro _lpPropTagArray_ debe ser NULL, que indica que se deben devolver los valores de todas las propiedades del objeto, o señalar a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una o más etiquetas de propiedad. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de marcadores que indica el formato para las propiedades que tengan el tipo de PT_UNSPECIFIED. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Los valores de cadena para estas propiedades se deben devolver en el formato Unicode. Si no está establecido el indicador MAPI_UNICODE., se deben devolver los valores de cadena en el formato ANSI.
    
 _lpcValues_
  
> [out] Un puntero a un recuento de valores de la propiedad indicada por el parámetro _lppPropArray_ . Si _lppPropArray_ es NULL, el contenido del parámetro _lpcValues_ es cero. 
    
 _lppPropArray_
  
> [out] Un puntero a un puntero a los valores de propiedad recuperado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los valores de propiedad se recuperaron correctamente.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada satisfactoria, pero no se podrían tener acceso a una o más propiedades. El miembro **aulPropTag** de para cada propiedad no está disponible el valor de la propiedad tiene un tipo de propiedad de PT_ERROR y un identificador de cero. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
MAPI_E_INVALID_PARAMETER 
  
> Cero se pasó en el miembro **cValues** de la estructura del **elemento SPropTagArray** que señala _lpPropTagArray_.
    
## <a name="remarks"></a>Notas

El método **IMAPIProp::GetProps** obtiene los valores de propiedad de una o varias propiedades de un objeto. 
  
Se devuelven los valores de propiedad en el mismo orden medida que se solicitan (es decir, el orden de las propiedades de la matriz de la etiqueta de propiedad que señala _lpPropTagArray_ coincidencias del orden de la matriz de estructuras de valor de propiedad que señala _lppPropArray _). 
  
Los tipos de propiedad especificados en los miembros de **aulPropTag** de la matriz de la etiqueta de propiedad indican el tipo de valor que se debe devolver en el miembro de **valor** de cada estructura de valor de propiedad. Sin embargo, si el autor de la llamada no conoce el tipo de una propiedad, el tipo en el miembro **aulPropTag** se puede establecer en su lugar en PT_UNSPECIFIED. Al recuperar el valor, **GetProps** establece el tipo correcto en el miembro **aulPropTag** de la estructura del valor de propiedad para la propiedad. 
  
Si se especifican los tipos de propiedad en el **elemento SPropTagArray** en _lpPropTagArray_, los valores de propiedad en la **SPropValue** devuelta en _lppPropArray_ tienen tipos que coincidan exactamente con los tipos solicitados, a menos que se devuelve un valor de error en su lugar. 
  
Propiedades de cadena pueden tener uno de los dos tipos de propiedad: PT_UNICODE para representar el formato Unicode y PT_STRING8 para representar el formato ANSI. Si se establece el indicador MAPI_UNICODE en el parámetro _ulFlags_ , siempre que **GetProps** no puede determinar el formato adecuado para una propiedad de cadena, devuelve su valor en el formato Unicode. **GetProps** no puede determinar un tipo de propiedad de cadena exacta en las situaciones siguientes: 
  
- El parámetro _lpPropTagArray_ se establece en NULL para solicitar todas las propiedades. 
    
- El miembro **aulPropTag** incluye el valor de PT_UNSPECIFIED como su tipo de propiedad en la matriz de la etiqueta de propiedad. 
    
Si el parámetro _lpPropTagArray_ se establece en NULL para recuperar todas las propiedades del objeto y no existen propiedades, **GetProps** hace lo siguiente: 
  
- Devuelve S_OK.
    
- Establece el valor de recuento en el miembro **cValues** de la estructura del valor de propiedad en 0. 
    
- Establece el contenido de _lpcValues_ en 0. 
    
- _LppPropArray_ se establece en NULL. 
    
 **GetProps** no debe devolver las propiedades de varios valores con **cValues** se establecen en 0. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Llame a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) para asignar memoria inicialmente para la estructura de [SPropValue](spropvalue.md) que señala _lpPropTagArray_; Llame a [MAPIAllocateMore](mapiallocatemore.md) para asignar cualquier memoria adicional necesaria para los miembros de estructura. 
  
Devolver MAPI_W_ERRORS_RETURNED si no se puede recuperar el valor de una o varias de las propiedades solicitadas. En la estructura del valor de propiedad, establezca el tipo en el miembro **aulPropTag** para PT_ERROR y el miembro de **valor** a un código de estado que describe el error. Por ejemplo, si tiene que convertir una cadena en Unicode y no admiten Unicode, establezca al miembro de **valor** a MAPI_E_BAD_CHARWIDTH. Si la propiedad es demasiado grande, establézcalo en MAPI_E_NOT_ENOUGH_MEMORY. Si el objeto no admite la propiedad, establézcalo en MAPI_E_NOT_FOUND. 
  
Implementación del proveedor de transporte remoto del método **GetProps** debe devolver los valores de propiedades de la carpeta de propiedades solicitados por el autor de la llamada. Su implementación debe hacer lo siguiente: 
  
- Asignar una matriz de valores de propiedad para volver al autor de la llamada y almacenar su dirección en el parámetro de puntero de valor de propiedad que se pasó para ese propósito.
    
- Copie las etiquetas de propiedad de las propiedades de la carpeta en las etiquetas de propiedad en la matriz de valores de propiedad según la matriz de etiquetas (propiedad) se pasan a **GetProps**.
    
- Asegúrese de que el tipo de propiedad se establece para todas las etiquetas de propiedad que se pasan a **GetProps**. El autor de la llamada puede pasar en un tipo de propiedad de PT_UNSPECIFIED, en el que caso **GetProps** debe establecer el tipo de propiedad correcto para esa etiqueta de propiedad. 
    
- Establezca el valor de cada propiedad de la matriz de valores de propiedad según su etiqueta. Por ejemplo, si la etiqueta de la propiedad solicitada por el autor de la llamada es **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** puede establecer el valor en MAPI_FOLDER. 
    
- Si el autor de la llamada pasa las etiquetas de propiedad que no controla su implementación, puede establecer la etiqueta de propiedad en PT_ERROR para esas propiedades y establezca el valor de propiedad en MAPI_E_NOT_FOUND.
    
- Devuelve S_OK si se ha producido ningún error ni MAPI_W_ERRORS_RETURNED si se han producido errores.
    
Implementación del proveedor de transporte remoto del método **GetProps** debe admitir las siguientes propiedades como mínimo: 
  
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

Para las propiedades de tipo pt Object, llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en lugar de **GetProps**. 
  
Para las propiedades seguras, no se espera recuperar al llamar a **GetProps** con el parámetro _lppPropTagArray_ establecido en NULL. Debe establecer explícitamente el identificador de la propiedad segura en el miembro **aulPropTag** de su matriz de etiqueta de propiedad cuando se llama a **GetProps**. Cómo y cuándo está disponible una propiedad segura es hasta el proveedor de servicios. 
  
Libere la estructura **SPropValue** devuelta por una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) sólo si **GetProps** devuelve S_OK o MAPI_W_ERRORS_RETURNED. 
  
Si **GetProps** devuelve MAPI_W_ERRORS_RETURNED porque no se pudo tener acceso una o más propiedades, compruebe las etiquetas de propiedad de las propiedades devueltas. Las propiedades con errores tendrá los siguientes valores establecidos en su estructura de valor de propiedad: 
  
- El tipo de propiedad en el miembro **aulPropTag** establecido en PT_ERROR. 
    
- El valor de la propiedad en el **valor de** conjunto de miembros a un código de estado para el error, como MAPI_E_NOT_FOUND. 
    
Las propiedades que se producirá un error porque son demasiado grandes para cómodamente se devuelven en la estructura de valor de propiedad tienen sus miembros **valor** establecido en MAPI_E_NOT_ENOUGH_MEMORY. Normalmente, este problema ocurre con las propiedades de tipo de cadena o binario PT_STRING8, PT_UNICODE o PT_BINARY cuando el valor de la propiedad es de 4 KB o más grande. Llame a **IMAPIProp::OpenProperty** para recuperar propiedades de gran tamaño. 
  
No todas las implementaciones de **GetProps** admiten formatos Unicode y ANSI para cadenas de caracteres. Cuando una propiedad concreta requiere la conversión de formato de cadena y **GetProps** no lo admiten, el miembro de **valor** de la propiedad se establece en MAPI_E_BAD_CHARWIDTH. 
  
Para comprobar si un archivo PST es un archivo PST de SharePoint, monte el PST utilizando [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), a continuación, se llame **GetProps** en el objeto de almacén de mensaje que solicita esta propiedad. Si existe, se puede suponer que se ha configurado el PST de SharePoint; Si no es así, el archivo PST no se ha configurado como un archivo PST de SharePoint. 
  
Para obtener más información acerca de cómo usar **GetProps** para tener acceso a las propiedades, vea [Recuperar propiedades de MAPI](retrieving-mapi-properties.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI utiliza el método **IMAPIProp::GetProps** para obtener todas las propiedades de un objeto pasando NULL o la matriz devuelta por el método [IMAPIProp::GetPropList](imapiprop-getproplist.md) en el parámetro _lpPropTagArray_ .  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Elemento SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Recuperación de propiedades MAPI](retrieving-mapi-properties.md)
  
[Usar Macros para el tratamiento de errores](using-macros-for-error-handling.md)

