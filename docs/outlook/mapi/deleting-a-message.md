---
title: Eliminar un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 663eebfcd1b8862b22d8c822957024c4f31499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433167"
---
# <a name="deleting-a-message"></a>Eliminar un mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un cliente puede eliminar un mensaje cuando está abierto y el usuario lo está leyendo, o cuando se cierra y el usuario está viendo la tabla de contenido. Para proteger a un usuario contra la eliminación involuntaria de un mensaje, MAPI define la eliminación de mensajes como un proceso de dos pasos:
  
1. Marque un mensaje para eliminarlo moviéndolo a la carpeta designada como carpeta Elementos eliminados, la carpeta cuyo identificador de entrada se almacena en la propiedad **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId).](pidtagipmwastebasketentryid-canonical-property.md) 
    
2. Quite el mensaje llamando al [método IMAPIFolder::D eleteMessages.](imapifolder-deletemessages.md) 
    
Cuando un usuario elija eliminar un mensaje en una carpeta que no sea la carpeta Elementos eliminados, marque esta opción para su eliminación. Solo cuando un usuario selecciona mensajes desde dentro de la carpeta Elementos eliminados debe quitar físicamente los mensajes de la estación de trabajo. Puede solicitar al usuario que compruebe que realmente tiene la intención de realizar la eliminación.
  
 **Para eliminar un mensaje**
  
1. Confirme con el usuario que la eliminación inminente es intencionada.
    
2. Determine el elemento principal de la carpeta que se va a eliminar. Si es la carpeta Elementos eliminados o una subcarpeta dentro de la carpeta Elementos eliminados, llame a [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md) para quitar el mensaje. 
    
3. Si la carpeta no está incluida en la carpeta Elementos eliminados, llame a [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) con la marca MESSAGE_MOVE establecida para reubicar el mensaje en la carpeta Elementos eliminados. 
    

