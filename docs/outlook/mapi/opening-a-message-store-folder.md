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
ms.openlocfilehash: 2ac4a30d6afc7e5245441bfe2d501169dd3a9447
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586126"
---
# <a name="opening-a-message-store-folder"></a>Abrir una carpeta de almacén de mensajes

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Antes de que se puede abrir cualquier carpeta, su identificador de entrada debe estar disponible. Para la mayoría de las carpetas, esto significa que la recuperación de sus propiedades de **entrada del objeto** . Para las carpetas especiales, como algunas de las carpetas del subárbol IPM y otras carpetas raíz, MAPI define las propiedades de identificador de entrada especiales que son accesibles mediante una llamada al método de **IMAPIProp::GetProps** del almacén de mensajes. Estos identificadores de entrada siempre son a largo plazo y se denominan de la siguiente manera: 
  
|**Folder**|**Propiedad de identificador de entrada**|
|:-----|:-----|
|Carpeta Bandeja de salida  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (Sólo clase de mensaje IPM)  <br/> |
|Carpeta Elementos eliminados  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|carpeta de elementos enviados  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|Carpeta ra�z IPM  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Carpeta ra�z de los resultados de b�squeda  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Carpeta raíz de vistas comunes  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Carpeta raíz de vistas personales  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Carpeta raíz de contactos  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Carpeta raíz de borradores  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Carpeta raíz de diario  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Carpeta raíz del calendario  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Notas de la carpeta raíz  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Carpeta raíz de tareas  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Antes de intentar recuperar uno de estos identificadores de entrada especiales, recuperar el **PR\_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) (propiedad) del almacén de mensajes. **PR\_VALID_FOLDER_MASK** es una máscara de bits que identifica qué de la entrada especial existen identificadores. Hay un bit para cada una de las carpetas especiales. Si está establecido el bit, indica que la carpeta correspondiente es compatible y que tiene un identificador de entrada válido. Por ejemplo, si existe la carpeta de elementos eliminados y tiene un identificador de entrada válido, la carpeta\_IPM_WASTEBASKET_VALID bit se establecerá en **PR_VALID_FOLDER_MASK**. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Abra la carpeta donde se colocan todos los mensajes entrantes de una clase determinada
  
1. Llame a [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar su identificador de entrada, si se establece el parámetro _lpszMessageClass_ para que apunte a una cadena de caracteres que identifica la clase de mensaje. Por ejemplo, si desea abrir la Bandeja de entrada para el subárbol IPM, elija _lpszMessageClass_ IPM. Si desea abrir la carpeta de recepción de mensajes IPC, establézcalo para que apunte a IPC. 

   Si no hay ninguna carpeta de recepción registrados para la clase de mensaje, **GetReceiveFolder** elige la carpeta de recepción cuya clase de mensaje asociado coincide con el prefijo más largo posible de la clase de mensaje que se pasó. Para obtener más información, vea [Carpetas reciben de MAPI](mapi-receive-folders.md). 
   
   Tenga en cuenta que la propiedad **PR_IPM_OUTBOX_ENTRYID** se usa para abrir la carpeta Bandeja de salida únicamente para los mensajes IPM. Si va a abrir la Bandeja de salida para los mensajes IPC, en su lugar, utilice el identificador de entrada para su carpeta de recepción. Los mensajes entrantes y salientes IPC se colocan en la carpeta de recepción. 
    
2. Llame a uno de los cuatro métodos **OpenEntry** para abrir la carpeta y devolver un puntero de interfaz que puede usar para obtener acceso a él. Se puede llamar a cualquiera de los métodos siguientes para abrir una carpeta: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   El método específico que elija dependerá de la carpeta que se va a abrir y los objetos que están disponibles en el momento. Debido a que el método **IMAPISession** puede abrir cualquier carpeta para cualquier almacén de mensajes en el perfil actual, llamar a este **OpenEntry** cuando no se sabe nada acerca de la carpeta que se va a abrir. Si sabe qué almacén de mensajes es propietario de la carpeta y tienen un puntero al almacén de mensajes, llamar a **IMsgStore::OpenEntry**. 
    
   Por ejemplo, use el método **IMsgStore** para abrir una carpeta de recepción. Si tiene un puntero al objeto de inicio de sesión del proveedor de almacén de mensajes, llamar a **IMSLogon::OpenEntry**. Debido a que estas llamadas vaya directamente al proveedor de almacén de mensajes en lugar de a través de MAPI, el procesamiento es más rápido. Si la carpeta que está abriendo es una subcarpeta de una carpeta que ya ha abierto, llamar al método open de la carpeta **IMAPIContainer::OpenEntry** . El método **IMAPIContainer** solo abre las subcarpetas de una carpeta se encuentra abierta actualmente y se garantiza que el único método para que funcione con los identificadores de entrada a corto plazo. 
    
3. Si desea que puedan realizar cambios en la carpeta que se abrirá, especifique un nivel de acceso estableciendo puede ser la de MAPI\_mejor\_acceso o MAPI\_indicador de modificar en la llamada **OpenEntry** . Estas marcas son sugerencias para el proveedor de almacenamiento de mensajes para conceder el mayor nivel de acceso, de MAPI\_mejor\_acceso o acceso de lectura y escritura, de MAPI\_modificar, al abrir la carpeta. 

   Debido a que estos marcadores sólo son sugerencias, la carpeta o no se puede abrir con el nivel de acceso que espera. Mediante la recuperación de la propiedad **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)), puede determinar el intervalo de operaciones que se pueden realizar en la carpeta abierta. 
    
   Sin embargo, debido a que muchos de los proveedores de almacén de mensajes calculen el valor de esta propiedad en propuestas, en lugar de dar soporte técnico como una propiedad de la carpeta o como una columna en su tabla de jerarquía, la recuperación se puede llevar mucho tiempo. Es una estrategia alternativa intentar cualquier operación que debe realizar y devolver un error si es necesario.
    
## <a name="see-also"></a>Vea también

- [Propiedad canónico PidTagEntryId](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

