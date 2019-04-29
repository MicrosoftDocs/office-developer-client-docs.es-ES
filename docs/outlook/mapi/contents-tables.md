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
  
Una tabla de contenido contiene información sobre los objetos de un contenedor de MAPI. Los proveedores de la libreta de direcciones implementan tablas de contenido para cada uno de sus contenedores, y los proveedores de almacenamiento de mensajes y de transporte remoto implementan tablas de contenido para sus carpetas. La tabla de contenido de un contenedor de libreta de direcciones muestra información sobre sus objetos de mensajería y de lista de distribución, mientras que la tabla de contenido de una carpeta muestra información sobre sus mensajes. Las tablas de contenido son utilizadas principalmente por las aplicaciones cliente. 
  
Hay dos tipos de tablas de contenido de carpetas:
  
- Las tablas de contenido estándar contienen mensajes estándar: los mensajes que se pueden transmitir y hacer visibles a un usuario. 
    
- Las tablas de contenido asociadas contienen información oculta y no transmitible creada por un cliente para un fin específico, como, por ejemplo, almacenar una representación alternativa de un mensaje estándar. La información asociada se crea pasando la marca MAPI_ASSOCIATED a la llamada a [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) . 
    
Las tablas de contenido de la mayoría de los contenedores de la libreta de direcciones y muchas carpetas no admiten la ordenación por categorías. 
  
Se puede tener acceso a una tabla de contenido llamando a:
  
- [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md).
    
    - O
    
- [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) con **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) o **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (sólo carpetas) especificados como la etiqueta de propiedad y IID _IMAPITable como identificador de interfaz.
    
Los proveedores de la libreta de direcciones y el almacén de mensajes deben admitir ambas técnicas para recuperar las propiedades de la tabla. No es aceptable que los proveedores admitan una sola forma de acceso a estas tablas porque los clientes esperan tener la elección. 
  
 **GetContentsTable** acepta como entrada varias marcas que especifican preferencias. Cuando se establece, la marca MAPI_ASSOCIATED recupera una tabla de contenido asociada. Como algunas carpetas no admiten el contenido asociado, y no hay forma de que los clientes determinen esta anticipación, **GetContentsTable** a veces devuelve el error MAPI_E_NO_SUPPORT cuando se solicita una tabla de contenido asociada. 
  
La marca MAPI_DEFERRED_ERRORS indica al implementador de la tabla que no es necesario notificar los errores encontrados durante la llamada en algún momento posterior. 
  
La llamada a **IMAPIProp:: OpenProperty** implica el acceso a una tabla de contenido abriendo su propiedad correspondiente, **PR_CONTAINER_CONTENTS** para las tablas de contenido de la libreta de direcciones y las tablas de contenido de la carpeta estándar, y **PR_FOLDER_ASSOCIATED_ CONTENIDO** de las tablas de contenido asociadas. Aunque ninguna o estas propiedades se pueden recuperar a través del método [IMAPIProp:: GetProps](imapiprop-getprops.md) de una carpeta o un contenedor, se incluyen en la matriz de etiquetas de propiedades devuelta por el método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_CONTENTS** también se puede usar para incluir o excluir una tabla de contenido de una operación de copia. Si un cliente especifica **PR_CONTAINER_CONTENTS** en el parámetro *lpExcludeProps* para **IMAPIProp:: CopyTo** en una operación de copia, la nueva carpeta o contenedor no admitirá la tabla de contenido del contenedor o la carpeta originales. 
  
Las tablas contenedor de la libreta de direcciones y contenido de la carpeta tienen una lista larga de columnas requeridas (columnas que los clientes pueden esperar que estén disponibles después de que recuperen la tabla de **GetContentsTable** o **OpenProperty**. Los proveedores pueden agregar este conjunto obligatorio si es necesario y los clientes, a través del método **SetColumns** , también pueden solicitar modificaciones. 
  
Las columnas necesarias para cada uno de los tipos de tablas de contenido son:
  
|**Columna obligatoria**|**Tipo de tabla de contenido**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Tablas del contenedor de libreta de direcciones  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Tablas del contenedor de libreta de direcciones  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Tablas del contenedor de libreta de direcciones  <br/> |
|**** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Todas las tablas de contenido  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Todas las tablas de contenido  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Tablas de carpetas de transporte remotas  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Todas las tablas de contenido  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Contenedor de libreta de direcciones y tablas de carpetas del almacén de mensajes  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Tablas de carpetas de transporte remotas  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
   
El identificador de entrada disponible con cada fila puede ser un identificador de entrada de corto o largo plazo, en función de la implementación de la tabla. Los identificadores de entrada a corto plazo se suelen usar en situaciones en las que el rendimiento es un problema. Cualquier tipo de identificador de entrada se puede usar para obtener acceso al objeto correspondiente. 
  
Las tablas de contenido también tienen un conjunto de columnas que son opcionales pero que suelen incluir los proveedores de servicios en sus implementaciones. Estas columnas opcionales son:
  
|**Columna opcional**|**Tipo de tabla de contenido**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Tablas de contenido de carpetas estándar  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Tablas de contenido de carpetas estándar  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Tablas de carpetas del almacén de mensajes  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Tablas del contenedor de libreta de direcciones  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Tablas del contenedor de libreta de direcciones  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Tablas del contenedor de libreta de direcciones  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Tablas de contenido de todas las carpetas  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Tablas del contenedor de libreta de direcciones  <br/> |
   
Los proveedores de almacenamiento de mensajes también deben incluir **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) para las tablas de contenido de las carpetas de resultados de búsqueda.
  
Las propiedades con nombre solo se pueden agregar al conjunto de columnas de una tabla de contenido de carpeta si todos los mensajes de la carpeta tienen la misma firma de asignación, es decir, la misma asignación de nombres de propiedad a los identificadores de propiedad. Las tablas contenido de la carpeta deben admitir la adición de propiedades específicas de clase de mensaje al conjunto de columnas, si admiten la creación de mensajes arbitrarios en la carpeta.
  
Los clientes pueden guardar el criterio de ordenación predeterminado para una tabla de contenido de carpeta llamando a su método [IMAPIFolder:: SaveContentsSort](imapifolder-savecontentssort.md) . Si se especifica la marca RECURSIVE_SORT en la llamada, el criterio de ordenación se puede aplicar a todas las subcarpetas de la carpeta. 
  
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

