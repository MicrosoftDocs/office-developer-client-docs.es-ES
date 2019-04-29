---
title: Abrir una carpeta de almacén de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: df7db013cb435484c721388abab51ab4ba43828f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436541"
---
# <a name="opening-a-message-store-folder"></a>Abrir una carpeta de almacén de mensajes

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Antes de que se pueda abrir cualquier carpeta, su identificador de entrada debe estar disponible. Para la mayoría de las carpetas, esto implica **** recuperar sus propiedades de no. Para las carpetas especiales, como algunas de las carpetas de subárbol IPM y otras carpetas raíz, MAPI define propiedades de identificador de entrada especiales a las que se puede tener acceso llamando al método **IMAPIProp:: GetProps** del almacén de mensajes. Estos identificadores de entrada son siempre a largo plazo y se denominan de la siguiente manera: 
  
|**Folder**|**Propiedad de identificador de entrada**|
|:-----|:-----|
|Carpeta Bandeja de salida  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (Solo clase de mensaje IPM)  <br/> |
|carpeta Elementos eliminados  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|carpeta de elementos enviados  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|Carpeta ra�z IPM  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Carpeta ra�z de los resultados de b�squeda  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Carpeta raíz de vistas comunes  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Carpeta raíz de vistas personales  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Carpeta raíz de contactos  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Carpeta raíz borradores  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Carpeta raíz del diario  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Carpeta raíz del calendario  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Carpeta raíz de notas  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Carpeta raíz de tareas  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Antes de intentar recuperar uno de estos identificadores de entrada especiales, recupere la propiedad **\_PR VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) del almacén de mensajes. **PR\_VALID_FOLDER_MASK** es una máscara de que identifica los identificadores de entrada especiales que existen. Hay un bit para cada una de las carpetas especiales. Si el bit está establecido, indica que la carpeta correspondiente es compatible y tiene un identificador de entrada válido. Por ejemplo, si la carpeta elementos eliminados existe y tiene un identificador de entrada válido, el\_bit IPM_WASTEBASKET_VALID de la carpeta se establecerá en **PR_VALID_FOLDER_MASK**. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Abrir la carpeta en la que se colocan todos los mensajes entrantes de una clase determinada
  
1. Llame a [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar su identificador de entrada, estableciendo el parámetro _lpszMessageClass_ para que apunte a una cadena de caracteres que identifica la clase de mensaje. Por ejemplo, si desea abrir la bandeja de entrada de su subárbol IPM, señale _lpszMessageClass_ a IPM. Si desea abrir la carpeta de recepción para los mensajes IPC, establézcalo para que apunte a IPC. 

   Si no hay ninguna carpeta de recepción registrada para la clase de mensaje, **GetReceiveFolder** elige la carpeta de recepción cuya clase de mensaje asociada coincide con el prefijo más largo posible de la clase de mensaje pasada. Para obtener más información, consulte [carpetas de recepción MAPI](mapi-receive-folders.md). 
   
   Tenga en cuenta que la propiedad **PR_IPM_OUTBOX_ENTRYID** se usa para abrir la carpeta Bandeja de salida sólo para los mensajes IPM. Si va a abrir la bandeja de salida de los mensajes IPC, use en su lugar el identificador de entrada de su carpeta de recepción. Los mensajes IPC entrantes y salientes se colocan en la carpeta de recepción. 
    
2. Llame a uno de los cuatro métodos de **OpenEntry** para abrir la carpeta y devolver un puntero de interfaz que puede usar para tener acceso a ella. Puede llamar a uno de los métodos siguientes para abrir una carpeta: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   El método específico que elija depende de la carpeta que se va a abrir y de los objetos que están disponibles en ese momento. Dado que el método **IMAPISession** puede abrir cualquier carpeta de cualquier almacén de mensajes en el perfil actual, llame a este **OpenEntry** cuando no sepa nada sobre la carpeta que se va a abrir. Si sabe qué almacén de mensajes es el propietario de la carpeta y tiene un puntero al almacén de mensajes, llame a **IMsgStore:: OpenEntry**. 
    
   Por ejemplo, use el método **IMsgStore** para abrir una carpeta de recepción. Si tiene un puntero al objeto de inicio de sesión del proveedor de almacenamiento de mensajes, llame a **IMSLogon:: OpenEntry**. Como estas llamadas se dirigen directamente al proveedor de almacenamiento de mensajes en lugar de a través de MAPI, el procesamiento es más rápido. Si la carpeta que está abriendo es una subcarpeta de una carpeta que ya tiene abierta, llame al método **IMAPIContainer:: OpenEntry** de la carpeta abierta. El método **IMAPIContainer** sólo abre las subcarpetas de una carpeta abierta actualmente y es el único método que se garantiza que funciona con los identificadores de entrada a corto plazo. 
    
3. Si desea poder realizar cambios en la carpeta que se va a abrir, especifique un nivel de acceso; para ello, configure\_el\_indicador de acceso\_de MAPI mejor o de modificación MAPI en la llamada **OpenEntry** . Estas marcas son sugerencias para que el proveedor de almacén de mensajes conceda el máximo nivel de acceso\_,\_para el mejor acceso de MAPI o el acceso de\_lectura y escritura para la modificación de MAPI, al abrir la carpeta. 

   Como estos marcadores solo son sugerencias, la carpeta puede o no abrirse con el nivel de acceso que esperaba. Al recuperar la propiedad **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)), puede determinar el intervalo de operaciones que se pueden realizar en la carpeta abierta. 
    
   Sin embargo, dado que muchos proveedores de almacenamiento de mensajes calculan el valor de esta propiedad a petición, en lugar de ser compatibles como una propiedad de carpeta o como una columna de la tabla de jerarquías, recuperarlo puede llevar mucho tiempo. Una estrategia alternativa es intentar cualquier operación que necesite realizar y devolver un error si es necesario.
    
## <a name="see-also"></a>Ver también

- [Propiedad canónica PidTagEntryId](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

