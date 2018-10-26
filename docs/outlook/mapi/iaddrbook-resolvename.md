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
ms.openlocfilehash: 1f09c88d9bd6720720e2d30ac24fa4a19aed5538
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567233"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Realiza la resolución de nombres, asignar los identificadores de entrada a los destinatarios en una lista de destinatarios.
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Un identificador de la ventana principal de un cuadro de diálogo que se muestra, si se especifica, para que solicite al usuario que resuelva la ambigüedad.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controlan los distintos aspectos del proceso de resolución. Se pueden establecer los siguientes indicadores:
    
AB_UNICODEUI
  
> Indica que _lpszNewEntryTitle_ es una cadena UNICODE. 
    
MAPI_CACHE_ONLY
  
> Usar sólo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
MAPI_DIALOG 
  
> Muestra un cuadro de diálogo para preguntar al usuario para la información de resolución de nombres adicionales. Si no se establece este marcador, no se muestra ningún cuadro de diálogo. 
    
MAPI_UNICODE 
  
> Indica que las propiedades devueltas en la lista de direcciones deben ser de tipo PT_UNICODE en lugar de PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> [entrada] Un puntero al texto del título del control en el cuadro de diálogo que solicita al usuario que escriba a un destinatario. El título varía según el tipo de destinatario. El parámetro _lpszNewEntryTitle_ puede ser NULL. 
    
 _lpAdrList_
  
> [entrada salida] Un puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de nombres de los destinatarios que se va a resolver. Esta estructura **ADRLIST** puede crearse mediante el método [IAddrBook::Address](iaddrbook-address.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proceso de resolución de nombres se ha realizado correctamente.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Al menos un destinatario en el parámetro _lpAdrList_ , coincidió con más de una entrada en la libreta de direcciones. Normalmente, este valor se devuelve cuando se establece la marca MAPI_DIALOG, prohibir la presentación de un cuadro de diálogo. 
    
MAPI_E_NOT_FOUND 
  
> No se puede resolver al menos un destinatario en el parámetro _lpAdrList_ . Normalmente, este valor se devuelve cuando se establece la marca MAPI_DIALOG, prohibir la presentación de un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios de llamar al método **ResolveName** para iniciar el proceso de resolución de nombres. Una entrada no resuelta es una entrada que aún no tiene una propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) o el identificador de entrada.
  
 **ResolveName** pasa por el proceso siguiente para cada entrada sin resolver en la lista de direcciones que se pasa en el parámetro _lpAdrList_ . 
  
1. Si el tipo de dirección del destinatario sigue el formato de una dirección SMTP ( _displayname_@ _dominio de nivel domain.top_), **ResolveName** le asigna un identificador de entrada único. 
    
2. Para cada contenedor de la propiedad **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** llama el método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . **ResolveNames** intenta hacer coincidir el nombre para mostrar de cada destinatario sin resolver con un nombre para mostrar que pertenece a uno de sus entradas. 
    
3. Si un contenedor no admite **ResolveNames**, **ResolveName** restringe la tabla de contenido del contenedor mediante el uso de una restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Esta restricción hace que el contenedor para llevar a cabo un tipo "mejor adivinar" de búsqueda para buscar a un destinatario coincidente. Todos los contenedores deben admitir la restricción de propiedad **PR_ANR** . 
    
4. Cuando un contenedor devuelve un destinatario que coincida con varios nombres, **ResolveName** muestra un cuadro de diálogo si se establece la marca MAPI_DIALOG, que permite al usuario seleccionar el nombre correcto. 
    
5. Si se ha llamado a todos los contenedores en la propiedad **PR_AB_SEARCH_PATH** y se ha encontrado ninguna coincidencia, el destinatario se quede sin resolver. 
    
Si uno o más destinatarios están sin resolver, **ResolveName** devuelve MAPI_E_NOT_FOUND. Si uno o más destinatarios tenían ambiguo resolución que no se pudo resolver con un cuadro de diálogo, o porque no se ha establecido el indicador MAPI_DIALOG, **ResolveName** devuelve MAPI_E_AMBIGUOUS_RECIP. Cuando algunos de los destinatarios son ambiguos y algunas no se puede resolver, **ResolveName** puede devolver cualquiera de estos valores de error. 
  
Si no se puede resolver un nombre, el cliente puede crear una dirección de uso único que tiene una dirección con un formato especial y el identificador de entrada. Para obtener más información acerca del formato de los identificadores de entrada único, vea [Identificadores de entrada de uso único](one-off-entry-identifiers.md). Para obtener más información acerca del formato de direcciones de uso único, consulte [Direcciones de uso único](one-off-addresses.md).
  
MAPI admite cadenas de caracteres Unicode para el **ADRLIST** y los nuevos parámetros de título de entrada a **ResolveName**; Si se establece el indicador MAPI_UNICODE., las siguientes propiedades se devuelven como tipo PT_UNICODE en las estructuras [ADRENTRY](adrentry.md) : 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Sin embargo, siempre se devuelve la propiedad de **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) mientras escribe PT_STRING8.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI utiliza el método **ResolveName** para resolver una dirección de uso único antes de agregar a un mensaje.  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI utiliza el método **ResolveName** para buscar una entrada de la libreta de direcciones por nombre para mostrar.  <br/> |
   
## <a name="see-also"></a>Vea también



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

