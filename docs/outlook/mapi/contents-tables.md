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
ms.openlocfilehash: 0dd79d9630837b5ec8a709d386ccc0db987dfb5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816566"
---
# <a name="contents-tables"></a>Tablas de contenido

  
  
**Hace referencia a**: Outlook 
  
Una tabla de contenido contiene información acerca de los objetos en un contenedor MAPI. Los proveedores de la libreta de direcciones implementan las tablas de contenido para cada uno de sus contenedores y almacén de mensajes y los proveedores de transporte remoto implementan las tablas de contenido para sus carpetas. En la tabla de contenido de un contenedor de la libreta de direcciones muestra información sobre sus objetos de lista de distribución mensajería, mientras que la tabla de contenido de una carpeta muestra información acerca de sus mensajes. Tablas de contenido se usan principalmente por las aplicaciones cliente. 
  
Hay dos tipos de tablas de contenido de carpeta:
  
- Tablas de contenido estándar contienen mensajes estándar: los mensajes que se pueden transmitir y hace visible a un usuario. 
    
- Tablas de contenido asociada contienen información oculta, que no sean transmisible creada por el cliente para un propósito específico, como para almacenar una representación alternativa de un mensaje estándar. Información asociada se crea pasando el indicador MAPI_ASSOCIATED a la llamada de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . 
    
Pueden clasificar el contenido de las tablas de la mayoría de los contenedores de la libreta de direcciones y muchas carpetas no admiten la ordenación. 
  
Puede tener acceso a una tabla de contenido mediante una llamada al:
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - O bien -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) o **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (sólo carpetas) especificado como la etiqueta de propiedad y IID _IMAPITable como el identificador de interfaz.
    
Almacén de mensajes y dirección de los proveedores de libreta deben admitir ambas técnicas para recuperar propiedades de la tabla. Es inaceptable para proveedores admitir sólo una manera para obtener acceso a estas tablas debido a que los clientes esperan tener la opción. 
  
 **GetContentsTable** acepta como entrada varios indicadores que especifican las preferencias. Cuando se establece la marca MAPI_ASSOCIATED recupera una tabla de contenido asociada. Debido a que algunas carpetas no admiten contenido asociado y no hay ninguna forma para que los clientes determinar esto con anterioridad, **GetContentsTable** a veces devuelve el error MAPI_E_NO_SUPPORT cuando se solicita una tabla de contenido asociada. 
  
El indicador MAPI_DEFERRED_ERRORS indica que el implementador de la tabla que no es necesario que los errores detectados durante la llamada se notifiquen hasta un momento posterior. 
  
La llamada a **IMAPIProp::OpenProperty** implica el acceso a una tabla de contenido abriendo su propiedad correspondiente, **PR_CONTAINER_CONTENTS** de **PR_FOLDER_ASSOCIATED_, tablas de contenido de la libreta de direcciones y las tablas de contenido de carpeta estándar CONTENIDO** para las tablas de contenido de asociados. Aunque ninguno o estas propiedades se pueden recuperar a través de una carpeta o un método de [IMAPIProp::GetProps](imapiprop-getprops.md) del contenedor, se incluyen en la matriz de etiqueta de propiedad que es devuelto por el método [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_CONTENTS** también puede utilizarse para incluir o excluir una tabla de contenido de una operación de copia. Si un cliente especifica **PR_CONTAINER_CONTENTS** en el parámetro *lpExcludeProps* para **IMAPIProp::CopyTo** en una operación de copia, el contenedor o la nueva carpeta no será compatible con la tabla de contenido de la carpeta original o el contenedor. 
  
Tablas de contenido contenedor y carpeta de la libreta de direcciones tienen una larga lista de columnas obligatorias: columnas que los clientes pueden esperar a estar disponible después de que recuperarán la tabla de **GetContentsTable** o **OpenProperty**. Proveedores pueden agregar a este conjunto requerido si es necesario y los clientes, mediante el método **SetColumns** , también pueden solicitar modificaciones. 
  
Las columnas necesarias para cada uno de los tipos de tablas de contenido son:
  
|**Columna necesaria**|**Tipo de tabla de contenido**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Tablas de carpeta de almacén de mensajes  <br/> |
|**PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
|**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Todas las tablas de contenido  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Todas las tablas de contenido  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Tablas de carpeta de almacén de mensajes  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Tablas de carpeta de almacén de mensajes  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Tablas de la carpeta de transporte remoto  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Todas las tablas de contenido  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Tablas de carpeta de almacén de mensajes  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Tablas de carpeta de almacén de mensajes y de contenedor de la libreta de direcciones  <br/> |
|**PR_SENT_REPRESENTING_NAME de MAPI** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Tablas de la carpeta de transporte remoto  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Tablas de carpeta de almacén de mensajes  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Tablas de carpeta de almacén de mensajes  <br/> |
   
El identificador de entrada disponible con cada fila puede ser un corto o largo plazo identificador de entrada, dependiendo de la implementación de la tabla. Los identificadores de entrada a corto plazo se suelen usar en situaciones donde el rendimiento es un problema. Cualquier tipo de identificador de entrada puede utilizarse para tener acceso al objeto correspondiente. 
  
Las tablas de contenido también tienen un conjunto de columnas que son opcionales pero se incluye con frecuencia por los proveedores de servicio en sus implementaciones. Estas columnas opcionales son:
  
|**Columna opcional**|**Tipo de tabla de contenido**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Tablas de carpeta de almacén de mensajes  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Tablas de contenido de carpeta estándar  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Tablas de contenido de carpeta estándar  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Tablas de carpeta de almacén de mensajes  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Todas las tablas de contenido de carpeta  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Tablas de contenedor de la libreta de direcciones  <br/> |
   
Los proveedores de almacén de mensajes también deben incluir **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) para las tablas de contenido de las carpetas de resultado de búsqueda solo.
  
Pueden agregarse propiedades con nombre para el conjunto de columnas de una tabla de contenido de carpeta sólo si todos los mensajes en la carpeta tienen la misma asignación firma, es decir, la misma asignación de nombres de propiedad a los identificadores de propiedad. Las tablas de contenido de carpeta deben admitir Agregar clase de mensaje establecen propiedades específicas de la columna, si son compatibles con la creación de mensajes arbitrarios en la carpeta.
  
Los clientes pueden guardar el criterio de ordenación predeterminado para una tabla de contenido de carpeta llamando a su método [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md) . Si se ha especificado el indicador RECURSIVE_SORT en la llamada, se puede establecer el criterio de ordenación que se debe aplicar a todas las subcarpetas dentro de la carpeta. 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

