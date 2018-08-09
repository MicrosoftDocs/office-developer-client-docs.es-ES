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
ms.openlocfilehash: ed87a2a6e3232cec492da6be032cf54cd66c3772
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817095"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**Hace referencia a**: Outlook 
  
Realiza la resolución de nombres para una o más entradas de destinatarios.
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a>Par�metros

 _lpPropTagArray_
  
> [entrada] Un puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que describe las propiedades que se deben incluir en la estructura [ADRLIST](adrlist.md) devuelta por el proveedor. Para solicitar el conjunto de propiedades predeterminadas de un proveedor, pase NULL en el parámetro _lpPropTagArray_ . 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de texto de las cadenas devueltas. Se pueden establecer los siguientes indicadores:
    
EMS_AB_ADDRESS_LOOKUP
  
> Se encontrará sólo coincidencias de dirección de proxy exacta; se omiten las coincidencias parciales. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
MAPI_CACHE_ONLY
  
> Sólo la libreta de direcciones sin conexión se usará para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para habilitar una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange. 
    
MAPI_UNICODE. 
  
> Las propiedades de la cadena devuelta se encuentran en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
 _lpAdrList_
  
> [entrada, salida] En la entrada, un puntero a una estructura **ADRLIST** que contiene la lista de los destinatarios que se puede resolver. En la salida, un puntero a una estructura **ADRLIST** que contiene los nombres resueltos. 
    
 _lpFlagList_
  
> [entrada, salida] Un puntero a una matriz de marcadores, cada marca correspondiente a una estructura [ADRENTRY](adrentry.md) en el parámetro _lpAdrList_ , que proporciona el estado de la operación de resolución de nombres para el destinatario. Las marcas en el parámetro _lpFlagList_ se encuentran en el mismo orden que las entradas de _lpAdrList_. Se pueden establecer los siguientes indicadores:
    
MAPI_AMBIGUOUS 
  
> El destinatario correspondiente se ha resuelto, pero no a un identificador de entrada único. No deben intentar resolver a este destinatario otros contenedores. 
    
MAPI_RESOLVED 
  
> Se ha resuelto el destinatario correspondiente a un identificador de entrada único. No deben intentar resolver a este destinatario otros contenedores. 
    
MAPI_UNRESOLVED 
  
> La entrada correspondiente no se ha resuelto. Otros contenedores deben intentar resolver a este destinatario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proceso de resolución de nombres fue correcto.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de la libreta de direcciones no es compatible con la resolución de nombres de forma masiva mediante el uso de este método.
    
## <a name="remarks"></a>Comentarios

El método **ResolveNames** intenta hacer coincidir a los destinatarios sin resolver de la matriz de entradas en el parámetro _lpAdrList_ a los destinatarios de este contenedor de la libreta de direcciones. Un destinatario sin resolver normalmente tiene sólo la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y, posiblemente, algunas otras propiedades. Un destinatario sin resolver no tiene la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y su marca correspondiente en el parámetro _lpFlagList_ se establece en MAPI_UNRESOLVED. Por el contrario, un destinatario resuelto siempre tiene al menos la propiedad de **entrada del objeto** además de otras propiedades, como **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**y **PR_ADDRTYPE** ([ PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
Resolución de nombres normalmente se inicia cuando un cliente llama al método [IAddrBook::ResolveName](iaddrbook-resolvename.md) . MAPI de Outlook responde llamando al método **ResolveNames** de cada contenedor de la libreta de direcciones incluida en la ruta de búsqueda de la libreta de direcciones, especificada por la propiedad **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)). Las entradas en el parámetro _lpAdrList_ incluyen a destinatarios ya resueltos porque están en contenedores para la que MAPI ya ha llamado **ResolveNames**, debido a que las entradas que aparece anteriormente en la ruta de acceso de búsqueda. 
  
Cada contenedor intenta resolver las entradas sin resolver de forma que coincidan con el nombre para mostrar del destinatario con el nombre para mostrar de uno de sus entradas. Cuando se encuentra una coincidencia única, **ResolveNames** agrega la propiedad de **entrada del objeto** y otras propiedades que se incluyen en el parámetro _lpPropTagArray_ a la entrada correspondiente en la estructura **ADRLIST** saliente. **ResolveNames** , a continuación, Establece la entrada en el parámetro _lpFlagList_ a MAPI_RESOLVED. Puede ser el identificador de entrada que se almacenan en la propiedad de **entrada del objeto** a corto plazo o a largo plazo. 
  
Después de todos los contenedores en la búsqueda de ruta de acceso ha intentado realizar el proceso de resolución de nombres, MAPI abre un cuadro de diálogo, si es posible, para preguntar al usuario para obtener ayuda y resolver los conflictos restantes. 
  
Los clientes también pueden usar la estructura **ADRLIST** devuelta en las llamadas al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

No son necesarios para admitir la resolución de nombres con el método **ResolveNames** . En su lugar, o además, se pueden admitir con la restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Si decide se basan en la restricción de **PR_ANR** para la resolución de nombres, puede devolver MAPI_E_NO_SUPPORT. For more information, see [Implementaci�n de la resoluci�n de nombres](implementing-name-resolution.md).
  
Establezca la entrada de marca de un destinatario en el parámetro _lpFlagList_ a MAPI_UNRESOLVED si el destinatario no coincide con ninguno de los destinatarios del contenedor. 
  
Cuando un destinatario coincide con varios destinatarios, establezca su marca en MAPI_AMBIGUOUS y no cambie su estructura **ADRENTRY** . 
  
MAPI requiere algunas propiedades para los destinatarios que se incluyen en la lista de destinatarios de un mensaje. Puede incluir en la estructura **ADRENTRY** como parte del proceso de resolución de nombre o esperar MAPI solicitar ellos con las llamadas a los métodos [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) y [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) . Puede eliminar estas llamadas adicionales y mejorar el rendimiento mediante la inclusión de las siguientes propiedades en las estructuras **ADRENTRY** de todos los destinatarios resueltos: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Si algunas de las propiedades en el parámetro _lpPropTagArray_ no están disponibles, normalmente debido a que la entrada de contenedor no es compatible con las propiedades y no se incluyen en el miembro **ADRENTRY** del destinatario de la estructura de **ADRLIST** : Establezca el tipo de propiedad de cada propiedad no está disponible en PT_ERROR. 
  
No quite todas las propiedades de la estructura **ADRENTRY** resuelve un destinatario. 
  
Si debe reemplazar en lugar de modificar una estructura **ADRENTRY** , libre de la estructura **ADRENTRY** original en primer lugar por llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, asignar la estructura **ADRENTRY** con [de sustitución MAPIAllocateBuffer](mapiallocatebuffer.md).
  
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

