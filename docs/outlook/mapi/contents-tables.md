---
title: Tablas de contenido
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 491381c771cae65e682acc8033b6558523847d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435589"
---
# <a name="contents-tables"></a>Tablas de contenido

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de contenido contiene información acerca de los objetos de un contenedor MAPI. Los proveedores de libretas de direcciones implementan tablas de contenido para cada uno de sus contenedores, y el almacén de mensajes y los proveedores de transporte remoto implementan tablas de contenido para sus carpetas. La tabla de contenido de un contenedor de libreta de direcciones contiene información sobre sus objetos de lista de distribución y usuario de mensajería, mientras que la tabla de contenido de una carpeta muestra información sobre sus mensajes. Las tablas de contenido las usan principalmente las aplicaciones cliente. 
  
Hay dos tipos de tablas de contenido de carpeta:
  
- Las tablas de contenido estándar contienen mensajes estándar: mensajes que se pueden transmitir y hacer visibles para un usuario. 
    
- Las tablas de contenido asociadas contienen información oculta no transmitible creada por un cliente para un propósito específico, como almacenar una representación alternativa de un mensaje estándar. La información asociada se crea pasando la marca MAPI_ASSOCIATED a la [llamada IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) 
    
Las tablas de contenido de la mayoría de los contenedores de libreta de direcciones y muchas carpetas no admiten la ordenación por categorías. 
  
Se puede tener acceso a una tabla de contenido llamando a:
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - O bien:
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) o **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (solo carpetas) especificado como la etiqueta de propiedad y IID_IMAPITable como identificador de interfaz.
    
Los proveedores de almacén de mensajes y libreta de direcciones deben admitir ambas técnicas para recuperar propiedades de tabla. No es aceptable que los proveedores admitan solo una forma de obtener acceso a estas tablas porque los clientes esperan tener la opción. 
  
 **GetContentsTable** acepta como entrada varias marcas que especifican preferencias. Cuando se establece, MAPI_ASSOCIATED marca recupera una tabla de contenido asociada. Dado que algunas carpetas no admiten contenido asociado y los clientes no pueden determinar esto con antelación, **GetContentsTable** a veces devuelve el error MAPI_E_NO_SUPPORT cuando se solicita una tabla de contenido asociada. 
  
La MAPI_DEFERRED_ERRORS indica al implementador de la tabla que los errores detectados durante la llamada no necesitan ser notificados hasta más adelante. 
  
La llamada a **IMAPIProp::OpenProperty** implica tener acceso a una tabla de contenido abriendo su propiedad correspondiente, **PR_CONTAINER_CONTENTS** para tablas de contenido de libreta de direcciones y tablas de contenido de carpeta estándar y **PR_FOLDER_ASSOCIATED_CONTENTS** para tablas de contenido asociadas. Aunque ninguna de estas propiedades se puede recuperar a través del método [IMAPIProp::GetProps](imapiprop-getprops.md) de una carpeta o contenedor, se incluyen en la matriz de etiquetas de propiedades que devuelve el método [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
  
 **PR_CONTAINER_CONTENTS** puede usarse para incluir o excluir una tabla de contenido de una operación de copia. Si un cliente especifica **PR_CONTAINER_CONTENTS** en el parámetro  *lpExcludeProps*  para **IMAPIProp::CopyTo** en una operación de copia, la nueva carpeta o contenedor no admitirá la tabla de contenido de la carpeta o contenedor original. 
  
Las tablas de contenido de carpeta y contenedor de la libreta de direcciones tienen una larga lista de columnas necesarias, columnas que los clientes pueden esperar que estén disponibles después de recuperar la tabla de **GetContentsTable** o **OpenProperty**. Los proveedores pueden agregar a este conjunto necesario si es necesario y los clientes, a través del **método SetColumns,** también pueden solicitar modificaciones. 
  
Las columnas necesarias para cada uno de los tipos de tablas de contenido son:
  
|**Columna obligatoria**|**Tipo de tabla de contenido**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Todas las tablas de contenido  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Todas las tablas de contenido  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Tablas de carpetas de transporte remoto  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Todas las tablas de contenido  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Tablas de carpetas contenedora de libreta de direcciones y almacén de mensajes  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Tablas de carpetas de transporte remoto  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
   
El identificador de entrada disponible con cada fila puede ser un identificador de entrada a corto o largo plazo, según la implementación de la tabla. Los identificadores de entrada a corto plazo se usan normalmente en situaciones en las que el rendimiento es un problema. Se puede usar cualquier tipo de identificador de entrada para tener acceso al objeto correspondiente. 
  
Las tablas de contenido también tienen un conjunto de columnas que son opcionales pero que los proveedores de servicios normalmente incluyen en sus implementaciones. Estas columnas opcionales son:
  
|**Columna opcional**|**Tipo de tabla de contenido**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Tablas de contenido de carpeta estándar  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Tablas de contenido de carpeta estándar  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Todas las tablas de contenido de carpetas  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
   
Los proveedores de almacenamiento de mensajes también **deben incluir PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) solo para tablas de contenido de carpetas de resultados de búsqueda.
  
Las propiedades con nombre se pueden agregar al conjunto de columnas de una tabla de contenido de carpeta solo si todos los mensajes de la carpeta tienen la misma firma de asignación, es decir, la misma asignación de nombres de propiedad a identificadores de propiedad. Las tablas de contenido de carpetas deben admitir la adición de propiedades específicas de clase de mensaje al conjunto de columnas, si admiten la creación de mensajes arbitrarios en la carpeta.
  
Los clientes pueden guardar el criterio de ordenación predeterminado para una tabla de contenido de carpeta llamando a su [método IMAPIFolder::SaveContentsSort.](imapifolder-savecontentssort.md) Si se RECURSIVE_SORT marca en la llamada, se puede aplicar el criterio de ordenación a todas las subcarpetas de la carpeta. 
  
## <a name="see-also"></a>Consulte también



[Tablas MAPI](mapi-tables.md)

