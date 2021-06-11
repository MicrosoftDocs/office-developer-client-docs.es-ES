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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408134"
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
  
> [in] Un identificador de la ventana principal de un cuadro de diálogo que se muestra, si se especifica, para pedir al usuario que resuelva la ambigüedad.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controlan varios aspectos del proceso de resolución. Se pueden establecer las siguientes marcas:
    
AB_UNICODEUI
  
> Indica que  _lpszNewEntryTitle es_ una cadena UNICODE. 
    
MAPI_CACHE_ONLY
  
> Use solo la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo de intercambio en caché y acceda a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Esta marca solo es compatible con el Exchange libreta de direcciones.
    
MAPI_DIALOG 
  
> Muestra un cuadro de diálogo para solicitar al usuario información adicional de resolución de nombres. Si no se establece esta marca, no se muestra ningún cuadro de diálogo. 
    
MAPI_UNICODE 
  
> Indica que las propiedades devueltas en la lista de direcciones deben ser de tipo PT_UNICODE en lugar de PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> [in] Puntero al texto del título del control en el cuadro de diálogo que solicita al usuario que escriba un destinatario. El título varía según el tipo de destinatario. El  _parámetro lpszNewEntryTitle_ puede ser NULL. 
    
 _lpAdrList_
  
> [entrada y salida] Puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de nombres de destinatarios que se va a resolver. El método [IAddrBook::Address](iaddrbook-address.md) puede crear esta estructura **ADRLIST.** 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proceso de resolución de nombres se ha correctamente.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Al menos un destinatario del parámetro  _lpAdrList_ coincide con más de una entrada de la libreta de direcciones. Normalmente, este valor se devuelve cuando se establece MAPI_DIALOG marca, lo que prohíbe la presentación de un cuadro de diálogo. 
    
MAPI_E_NOT_FOUND 
  
> Al menos un destinatario del  _parámetro lpAdrList_ no se puede resolver. Normalmente, este valor se devuelve cuando se establece MAPI_DIALOG marca, lo que prohíbe la presentación de un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios llaman al **método ResolveName** para iniciar el proceso de resolución de nombres. Una entrada sin resolver es una entrada que aún no tiene un identificador de entrada o una propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
 **ResolveName** pasa por el siguiente proceso para cada entrada sin resolver de la lista de direcciones pasada en el _parámetro lpAdrList._ 
  
1. Si el tipo de dirección del destinatario se adhiere al formato de una dirección SMTP ( _displayname_ @  _domain.top-level-domain),_ **ResolveName** le asigna un identificador de entrada único. 
    
2. Para cada contenedor de **la propiedad PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** llama al [método IABContainer::ResolveNames.](iabcontainer-resolvenames.md) **ResolveNames intenta** hacer coincidir el nombre para mostrar de cada destinatario sin resolver con un nombre para mostrar que pertenece a una de sus entradas. 
    
3. Si un contenedor no admite **ResolveNames**, **ResolveName** restringe la tabla de contenido del contenedor mediante una restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Esta restricción hace que el contenedor realice un tipo de búsqueda de "mejor conjetura" para buscar un destinatario que coincida. Todos los contenedores deben admitir la **PR_ANR** de propiedades. 
    
4. Cuando un contenedor devuelve un destinatario que coincide con varios nombres, **ResolveName** muestra un cuadro de diálogo si se establece la marca MAPI_DIALOG, lo que permite al usuario seleccionar el nombre correcto. 
    
5. Si se ha llamado a todos los contenedores de **la propiedad PR_AB_SEARCH_PATH** y no se ha encontrado ninguna coincidencia, el destinatario permanece sin resolver. 
    
Si uno o varios destinatarios no están resueltos, **ResolveName** devuelve MAPI_E_NOT_FOUND. Si uno o varios destinatarios tenían una resolución ambigua que no se pudo resolver con un cuadro de diálogo o porque no se estableció la marca MAPI_DIALOG, **ResolveName** devuelve MAPI_E_AMBIGUOUS_RECIP. Cuando algunos de los destinatarios son ambiguos y otros no se pueden resolver, **ResolveName** puede devolver cualquiera de los dos valores de error. 
  
Si no se puede resolver un nombre, el cliente puede crear una dirección única que tenga una dirección con formato especial y un identificador de entrada. Para obtener más información sobre el formato de los identificadores de entrada únicos, vea [One-Off Entry Identifiers](one-off-entry-identifiers.md). Para obtener más información sobre el formato de las direcciones de uso único, vea [One-Off Addresses](one-off-addresses.md).
  
MAPI admite cadenas de caracteres Unicode para **ADRLIST** y los nuevos parámetros de título de entrada en **ResolveName**; si establece la marca MAPI_UNICODE, las siguientes propiedades se devuelven como tipo PT_UNICODE en las estructuras [ADRENTRY:](adrentry.md) 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Sin embargo, **la PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) siempre se devuelve como tipo PT_STRING8.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa el **método ResolveName** para resolver una dirección única antes de agregarla a un mensaje.  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI usa el **método ResolveName** para buscar una entrada de libreta de direcciones por nombre para mostrar.  <br/> |
   
## <a name="see-also"></a>Vea también



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

