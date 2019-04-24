---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287010"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza la resolución de nombres, asignando identificadores de entrada a los destinatarios de una lista de destinatarios.
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> a Identificador de la ventana primaria de un cuadro de diálogo que se muestra, si se especifica, para solicitar al usuario que resuelva la ambigüedad.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla diversos aspectos del proceso de resolución. Se pueden establecer los siguientes indicadores:
    
AB_UNICODEUI
  
> Indica que _lpszNewEntryTitle_ es una cadena Unicode. 
    
MAPI_CACHE_ONLY
  
> Use solo la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.
    
MAPI_DIALOG 
  
> Muestra un cuadro de diálogo para pedir al usuario información adicional sobre la resolución de nombres. Si no se establece esta marca, no se muestra ningún cuadro de diálogo. 
    
MAPI_UNICODE 
  
> Indica que las propiedades devueltas en la lista de direcciones deben ser del tipo PT_UNICODE en lugar de PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> a Un puntero al texto del título del control en el cuadro de diálogo que solicita al usuario que escriba un destinatario. El título varía en función del tipo de destinatario. El parámetro _lpszNewEntryTitle_ puede ser null. 
    
 _lpAdrList_
  
> [in-out] Un puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de nombres de destinatarios que se van a resolver. Esta estructura **ADRLIST** puede crearse mediante el método [IAddrBook:: Address](iaddrbook-address.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proceso de resolución de nombres se realizó correctamente.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Al menos un destinatario en el parámetro _lpAdrList_ coincide con más de una entrada de la libreta de direcciones. Normalmente, este valor se devuelve cuando se establece la marca MAPI_DIALOG, lo que prohíbe que se muestre un cuadro de diálogo. 
    
MAPI_E_NOT_FOUND 
  
> Al menos un destinatario en el parámetro _lpAdrList_ no se puede resolver. Normalmente, este valor se devuelve cuando se establece la marca MAPI_DIALOG, lo que prohíbe que se muestre un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Los clientes y los proveedores de servicios llaman al método **ResolveName** para iniciar el proceso de resolución de nombres. Una entrada no resuelta es una entrada que todavía no tiene una propiedad de identificador de entrada **** o de[PidTagEntryId](pidtagentryid-canonical-property.md)).
  
 **ResolveName** pasa por el proceso siguiente para cada entrada no resuelta en la lista de direcciones que se pasa en el parámetro _lpAdrList_ . 
  
1. Si el tipo de dirección del destinatario sigue el formato de una dirección SMTP ( _displayName_@ _Domain. Top-Domain-Domain_), **ResolveName** le asigna un identificador de entrada de un solo uso. 
    
2. Para cada contenedor de la propiedad **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** llama al método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . **ResolveNames** intenta hacer coincidir el nombre para mostrar de cada destinatario sin resolver con un nombre para mostrar que pertenece a una de sus entradas. 
    
3. Si un contenedor no admite **ResolveNames**, **ResolveName** restringe la tabla de contenido del contenedor mediante una restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Esta restricción hace que el contenedor realice un tipo de búsqueda "mejor estimación" para encontrar un destinatario que coincida. Todos los contenedores deben admitir la restricción de propiedad **PR_ANR** . 
    
4. Cuando un contenedor devuelve un destinatario que coincide con varios nombres, **ResolveName** muestra un cuadro de diálogo si se establece la marca MAPI_DIALOG, lo que permite al usuario seleccionar el nombre correcto. 
    
5. Si se ha llamado a todos los contenedores de la propiedad **PR_AB_SEARCH_PATH** y no se ha encontrado ninguna coincidencia, el destinatario sigue sin resolverse. 
    
Si no se resuelven uno o más destinatarios, **ResolveName** devuelve MAPI_E_NOT_FOUND. Si uno o más destinatarios tienen una resolución ambigua que no se pudo resolver con un cuadro de diálogo, o porque no se estableció la marca MAPI_DIALOG, **ResolveName** devuelve MAPI_E_AMBIGUOUS_RECIP. Cuando algunos de los destinatarios son ambiguos y algunos no se pueden resolver, **ResolveName** puede devolver cualquier valor de error. 
  
Si no se puede resolver un nombre, el cliente puede crear una dirección de uso único que tenga un identificador de entrada y una dirección con un formato especial. Para obtener más información acerca del formato de los identificadores de entrada de un solo uso, consulte identificadores de [entrada de un solo uso](one-off-entry-identifiers.md). Para obtener más información acerca del formato de las direcciones de uso único, consulte [direcciones de uso único](one-off-addresses.md).
  
MAPI admite las cadenas de caracteres Unicode para **ADRLIST** y los nuevos parámetros de título de entrada a **ResolveName**; Si establece la marca MAPI_UNICODE, se devuelven las siguientes propiedades como PT_UNICODE de tipo en las estructuras [ADRENTRY](adrentry.md) : 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Sin embargo, la propiedad **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) siempre se devuelve como tipo PT_STRING8.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIABFunctions. cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa el método **ResolveName** para resolver una dirección de un solo uso antes de agregarla a un mensaje.  <br/> |
|MAPIABFunctions. cpp  <br/> |AddRecipient  <br/> |MFCMAPI usa el método **ResolveName** para buscar una entrada de la libreta de direcciones por su nombre para mostrar.  <br/> |
   
## <a name="see-also"></a>Vea también



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

