---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fac4978bef94650f85ac3179acd3858602f933ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405817"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza la resolución de nombres de una o varias entradas de destinatarios.
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a>Parameters

 _lpPropTagArray_
  
> a Un puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que describe las propiedades que se van a incluir en la estructura [ADRLIST](adrlist.md) devuelta por el proveedor. Para solicitar el conjunto predeterminado de propiedades del proveedor, pase NULL en el parámetro _lpPropTagArray_ . 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el tipo de texto en las cadenas devueltas. Se pueden establecer los siguientes indicadores:
    
EMS_AB_ADDRESS_LOOKUP
  
> Solo se encuentran coincidencias exactas de direcciones de proxy; se omiten las coincidencias parciales. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.
    
MAPI_CACHE_ONLY
  
> Solo se usará la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange. 
    
MAPI_UNICODE 
  
> Las propiedades de cadena devueltas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
 _lpAdrList_
  
> [in, out] En la entrada, un puntero a una estructura **ADRLIST** que contiene la lista de los destinatarios que se van a resolver. En la salida, un puntero a una estructura **ADRLIST** que contiene los nombres resueltos. 
    
 _lpFlagList_
  
> [in, out] Un puntero a una matriz de indicadores, cada indicador correspondiente a una estructura [ADRENTRY](adrentry.md) en el parámetro _lpAdrList_ , que proporciona el estado de la operación de resolución de nombres para el destinatario. Las marcas del parámetro _lpFlagList_ están en el mismo orden que las entradas de _lpAdrList_. Se pueden establecer los siguientes indicadores:
    
MAPI_AMBIGUOUS 
  
> Se ha resuelto el destinatario correspondiente, pero no un identificador de entrada único. Otros contenedores no deben intentar resolver este destinatario. 
    
MAPI_RESOLVED 
  
> El destinatario correspondiente se ha resuelto en un identificador de entrada único. Otros contenedores no deben intentar resolver este destinatario. 
    
MAPI_UNRESOLVED 
  
> No se ha resuelto la entrada correspondiente. Otros contenedores deben intentar resolver este destinatario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proceso de resolución de nombres se realizó correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de la libreta de direcciones no admite la resolución de nombres en masa mediante este método.
    
## <a name="remarks"></a>Comentarios

El método **ResolveNames** intenta hacer coincidir los destinatarios sin resolver de la matriz de entradas en el parámetro _lpAdrList_ con los destinatarios de este contenedor de libretas de direcciones. Un destinatario sin resolver suele tener sólo la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y, posiblemente, algunas otras propiedades. Un destinatario sin resolver no tiene la propiedad de **** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y su marca correspondiente en el parámetro _lpFlagList_ se establece en MAPI_UNRESOLVED. Por el contrario, un destinatario resuelto siempre tiene al menos la **** propiedad del tipo de propiedad más otras propiedades, como **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**y **PR_ADDRTYPE** ([ PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
La resolución de nombres suele iniciarse cuando un cliente llama al método [IAddrBook:: ResolveName](iaddrbook-resolvename.md) . MAPI de Outlook responde llamando al método **ResolveNames** de cada contenedor de libretas de direcciones incluido en la ruta de acceso de búsqueda de la libreta de direcciones, especificada por la propiedad **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)). Las entradas del parámetro _lpAdrList_ incluyen los destinatarios que ya se han resuelto porque están en contenedores para los que MAPI ya ha llamado a **ResolveNames**, porque las entradas aparecen antes en la ruta de búsqueda. 
  
Cada contenedor intenta resolver las entradas sin resolver haciendo coincidir el nombre para mostrar del destinatario con el nombre para mostrar de una de sus entradas. Cuando se encuentra una coincidencia única, **ResolveNames** agrega la **** propiedad número y otras propiedades que se incluyen en el parámetro _lpPropTagArray_ a la entrada correspondiente en la estructura **ADRLIST** de salida. A continuación, **ResolveNames** establece la entrada en el parámetro _lpFlagList_ en MAPI_RESOLVED. El identificador de entrada almacenado en la **** propiedad o puede ser a corto o largo plazo. 
  
Una vez que todos los contenedores de la ruta de acceso de búsqueda han intentado realizar el proceso de resolución de nombres, MAPI abre un cuadro de diálogo, si es posible, para solicitar ayuda al usuario para resolver los conflictos restantes. 
  
Los clientes también pueden usar la estructura **ADRLIST** devuelta en llamadas al método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) . 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

No es necesario que admita la resolución de nombres con el método **ResolveNames** . En su lugar, o también puede admitirla con la restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Si decide utilizar la restricción **PR_ANR** para la resolución de nombres, puede devolver MAPI_E_NO_SUPPORT. For more information, see [Implementaci�n de la resoluci�n de nombres](implementing-name-resolution.md).
  
Establezca la entrada de la marca del destinatario en el parámetro _lpFlagList_ en MAPI_UNRESOLVED si el destinatario no coincide con ninguno de los destinatarios del contenedor. 
  
Cuando un destinatario coincide con varios destinatarios, establezca su indicador en MAPI_AMBIGUOUS y no cambie su estructura **ADRENTRY** . 
  
MAPI requiere ciertas propiedades para los destinatarios incluidos en la lista de destinatarios de un mensaje. Puede incluirlos en la estructura **ADRENTRY** como parte del proceso de resolución de nombres o esperar a que MAPI los solicite con llamadas a los métodos [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) y [IMAPISupport:: ExpandRecips](imapisupport-expandrecips.md) . Puede eliminar estas llamadas adicionales y mejorar el rendimiento si incluye las siguientes propiedades en las estructuras **ADRENTRY** de todos los destinatarios resueltos: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Si algunas de las propiedades del parámetro _lpPropTagArray_ no están disponibles, normalmente porque la entrada del contenedor no admite las propiedades y no se incluyen en el miembro **ADRENTRY** del destinatario en la estructura **ADRLIST** : Establezca el tipo de propiedad de cada propiedad no disponible en PT_ERROR. 
  
No quite ninguna propiedad de la estructura **ADRENTRY** de un destinatario resuelto. 
  
Si debe reemplazar en lugar de modificar una estructura **ADRENTRY** , libere primero la estructura **ADRENTRY** original llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, asigne la estructura **ADRENTRY** de reemplazo por [ MAPIAllocateBuffer](mapiallocatebuffer.md).
  
## <a name="see-also"></a>Ver también



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Propiedad canónica PidTagAnr](pidtaganr-canonical-property.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

