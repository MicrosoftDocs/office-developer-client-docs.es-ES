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
  
Realiza la resolución de nombres para una o más entradas de destinatarios.
  
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
  
> [in] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedades que describen las propiedades que se incluirán en la estructura [ADRLIST](adrlist.md) devuelta por el proveedor. Para solicitar el conjunto predeterminado de propiedades del proveedor, pase NULL en el _parámetro lpPropTagArray._ 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de texto de las cadenas devueltas. Se pueden establecer las siguientes marcas:
    
EMS_AB_ADDRESS_LOOKUP
  
> Solo se encontrarán coincidencias exactas de direcciones proxy; se omiten las coincidencias parciales. Esta marca solo es compatible con el Exchange libreta de direcciones.
    
MAPI_CACHE_ONLY
  
> Solo se usará la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo de intercambio en caché y obtenga acceso a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Esta marca solo es compatible con el Exchange libreta de direcciones. 
    
MAPI_UNICODE 
  
> Las propiedades de cadena devueltas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.
    
 _lpAdrList_
  
> [in, out] En la entrada, un puntero a una **estructura ADRLIST** que contiene la lista de destinatarios que se va a resolver. En el resultado, un puntero a una **estructura ADRLIST** que contiene los nombres resueltos. 
    
 _lpFlagList_
  
> [in, out] Puntero a una matriz de marcas, cada marca correspondiente a una estructura [ADRENTRY](adrentry.md) en el parámetro  _lpAdrList,_ que proporciona el estado de la operación de resolución de nombres para el destinatario. Las marcas del parámetro  _lpFlagList_ están en el mismo orden que las entradas de  _lpAdrList_. Se pueden establecer las siguientes marcas:
    
MAPI_AMBIGUOUS 
  
> El destinatario correspondiente se ha resuelto, pero no a un identificador de entrada único. Otros contenedores no deben intentar resolver este destinatario. 
    
MAPI_RESOLVED 
  
> El destinatario correspondiente se ha resuelto en un identificador de entrada único. Otros contenedores no deben intentar resolver este destinatario. 
    
MAPI_UNRESOLVED 
  
> La entrada correspondiente no se ha resuelto. Otros contenedores deben intentar resolver este destinatario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proceso de resolución de nombres se ha realizado correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de libreta de direcciones no admite la resolución masiva de nombres mediante este método.
    
## <a name="remarks"></a>Comentarios

El **método ResolveNames** intenta hacer coincidir los destinatarios no resueltos de la matriz de entradas del parámetro  _lpAdrList_ con los destinatarios de este contenedor de libreta de direcciones. Un destinatario no resuelto normalmente solo tiene la **propiedad PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y posiblemente algunas otras propiedades. Un destinatario no resuelto no tiene la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y su marca correspondiente en el parámetro  _lpFlagList_ se establece en MAPI_UNRESOLVED. Por el contrario, un destinatario resuelto siempre tiene al menos la propiedad **PR_ENTRYID** más otras propiedades, como **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME** y **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
La resolución de nombres normalmente se inicia cuando un cliente llama al [método IAddrBook::ResolveName.](iaddrbook-resolvename.md) Outlook MAPI responde llamando al método **ResolveNames** de cada contenedor de libreta de direcciones incluido en la ruta de búsqueda de la libreta de direcciones, especificado por la propiedad **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)). Las entradas del parámetro  _lpAdrList_ incluyen destinatarios ya resueltos porque están en contenedores para los que MAPI ya ha llamado **ResolveNames**, porque las entradas aparecen anteriormente en la ruta de búsqueda. 
  
Cada contenedor intenta resolver las entradas no resueltas haciendo coincidir el nombre para mostrar del destinatario con el nombre para mostrar de una de sus entradas. Cuando se encuentra una coincidencia única, **ResolveNames** agrega la propiedad PR_ENTRYID y otras propiedades que se incluyen en el parámetro _lpPropTagArray_ **a** la entrada correspondiente de la estructura **ADRLIST saliente.** **ResolveNames,** a continuación, establece la entrada en el  _parámetro lpFlagList_ en MAPI_RESOLVED. El identificador de entrada almacenado en **la propiedad PR_ENTRYID** puede ser a corto o largo plazo. 
  
Después de que todos los contenedores de la ruta de búsqueda han intentado el proceso de resolución de nombres, MAPI abre un cuadro de diálogo, si es posible, para solicitar ayuda al usuario para resolver los conflictos restantes. 
  
Los clientes también pueden usar la estructura **ADRLIST devuelta** en llamadas al [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md) 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

No es necesario admitir la resolución de nombres con el **método ResolveNames.** En su lugar, o además, puede admitirlo con la restricción de **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Si decide confiar en la restricción de PR_ANR **para** la resolución de nombres, puede devolver MAPI_E_NO_SUPPORT. For more information, see [Implementaci�n de la resoluci�n de nombres](implementing-name-resolution.md).
  
Establezca la entrada de marca de un destinatario en el parámetro  _lpFlagList_ en MAPI_UNRESOLVED si el destinatario no coincide con ninguno de los destinatarios del contenedor. 
  
Cuando un destinatario coincida con varios destinatarios, establezca su marca en MAPI_AMBIGUOUS y no cambie su **estructura ADRENTRY.** 
  
MAPI requiere ciertas propiedades para los destinatarios que se incluyen en la lista de destinatarios de un mensaje. Puede incluirlos en la estructura **ADRENTRY** como parte del proceso de resolución de nombres o esperar a que MAPI los solicite con llamadas a los métodos [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) e [IMAPISupport::ExpandRecips.](imapisupport-expandrecips.md) Puede eliminar estas llamadas adicionales y mejorar el rendimiento al incluir las siguientes propiedades en las estructuras **ADRENTRY** de todos los destinatarios resueltos: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Si algunas de las propiedades del parámetro  _lpPropTagArray_ no están disponibles,normalmente porque la entrada de contenedor no admite las propiedades y no se incluyen en el miembro **ADRENTRY** del destinatario en la estructura **ADRLIST,** establezca el tipo de propiedad de cada propiedad no disponible en PT_ERROR. 
  
No quite ninguna propiedad de la estructura **ADRENTRY de** un destinatario resuelto. 
  
Si debe reemplazar en lugar de modificar una estructura **ADRENTRY,** primero debe liberar la estructura **ADRENTRY** original llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, asigne la estructura **ADRENTRY** de reemplazo con [MAPIAllocateBuffer](mapiallocatebuffer.md).
  
## <a name="see-also"></a>Vea también



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Propiedad canónica PidTagAnr](pidtaganr-canonical-property.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

