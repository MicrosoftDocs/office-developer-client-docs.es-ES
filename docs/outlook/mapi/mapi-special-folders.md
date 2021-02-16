---
title: Carpetas especiales de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2aa2376-b293-4d05-9104-218cc1fe1758
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: fa221510a5f6a8c8be24b4869960d1770cef5882
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410927"
---
# <a name="mapi-special-folders"></a>Carpetas especiales de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI define algunas carpetas especiales porque sirven roles predefinidos como carpetas predeterminadas para determinados tipos de mensajes. Estas carpetas especiales normalmente no se puede eliminar, y tienen propiedades de identificador de entrada especial.
  
Existen ocho carpetas especiales, algunos que forman parte del sub�rbol de mensajes interpersonales (IPM). MAPI crea estas carpetas antes de que un cliente recibe acceso a su almac�n de mensajes, despu�s de que el cliente es posible que pueda eliminar las carpetas, si es necesario. Algunos proveedores de almac�n de mensajes permiten la eliminaci�n, mientras que otros no lo hacen. En la siguiente tabla se describe estas carpetas.
  
**Carpetas de MAPI**

|**Carpeta**|**Description**|
|:-----|:-----|
|Carpeta Bandeja de salida  <br/> |Contiene los mensajes salientes de IPM.  <br/> |
|Carpeta Elementos eliminados  <br/> |Contiene los mensajes IPM que est�n marcados para eliminaci�n.  <br/> |
|carpeta de elementos enviados  <br/> |Contiene los mensajes IPM que se han enviado.  <br/> |
|Carpeta ra�z IPM  <br/> |Contiene carpetas para administrar los mensajes IPM.  <br/> |
|Carpeta de recepci�n  <br/> |Contiene los mensajes entrantes para una clase de mensaje en particular.  <br/> |
|Carpeta ra�z de los resultados de b�squeda  <br/> |Contiene carpetas para administrar los resultados de b�squeda.  <br/> |
|Carpeta ra�z de vistas com�n  <br/> |Contiene carpetas para administrar las vistas para el almac�n de mensajes.  <br/> |
|Carpeta ra�z de vistas personales  <br/> |Contiene carpetas para administraci�n de vistas para un usuario determinado.  <br/> |
   
The first four folders relate to the IPM subtree, a tree of folders that MAPI creates when a message store is initialized. Default message stores for interactive messaging clients always include the IPM folder subtree and the other special folders in their folder hierarchy. Non-default message stores are required only to support the search-results root folder, the IPM subtree root folder, the Deleted Items folder, and the receive folder. To ensure that the IPM subtree folders exist and are valid, clients can call the [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function. **HrValidateIPMSubtree** checks the folders and recreates them if there is a problem. 
  
Las carpetas ra�z para las vistas personales, vistas comunes y los resultados de b�squeda no forman parte del sub�rbol IPM; Estas carpetas se crean en la carpeta ra�z para el almac�n de mensajes. La carpeta ra�z de los resultados de b�squeda contiene las carpetas que admiten las tablas de contenido con los mensajes que cumplen un conjunto de criterios de b�squeda. Aunque se permiten a los clientes para crear carpetas de resultados de b�squeda en cualquier carpeta, la mayor�a de los clientes designa una sola carpeta ra�z para ser el primario de todos los resultados de b�squeda carpetas creadas durante la sesi�n. 
  
Las carpetas de ra�z com�n vistas y vistas personales contienen los mensajes que describen las vistas o m�todos preferidos de presentar los datos de mensajes y carpetas. La carpeta ra�z de vistas de common contiene vistas que pueden usar los clientes con cualquier carpeta en el almac�n de mensajes; la carpeta vistas personales contiene vistas que se han definido por un usuario concreto para una carpeta o carpetas.
  
Los clientes que funcionan con los mensajes de IPM deben crear todas las carpetas y los mensajes en la carpeta ra�z del sub�rbol IPM, en lugar de la carpeta ra�z del almac�n de mensajes. Esto proporciona a los clientes no IPM: los clientes que abordar los problemas con los mensajes que se intercambian entre equipos o entre personas y equipos, un m�todo sencillo para ocultar sus mensajes de clientes IPM. 
  
MAPI assigns special entry identifier properties for these special folders. For a list of the special folder entry identifiers, see [Abrir una carpeta de almac�n de mensajes](opening-a-message-store-folder.md).
  
### <a name="outlook-special-folders"></a>Carpetas especiales de Outlook

Las carpetas especiales de Outlook se identifican mediante su identificadores que se almacenan en la carpeta Bandeja de entrada y la carpeta ra�z para el almac�n de mensajes de entrada.
  
|**Folder**|**La propiedad para establecer**|
|:-----|:-----|
|Calendar  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Contactos  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Diario  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Notas  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Tareas  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
|Borradores  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Consulte también



[Carpetas de MAPI](mapi-folders.md)

