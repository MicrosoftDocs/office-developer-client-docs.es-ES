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
ms.openlocfilehash: ad891a9884e72aa352dc114232cd5951c590272f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585104"
---
# <a name="deleting-a-message"></a>Eliminar un mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un cliente puede eliminar un mensaje cuando está abierto y el usuario lo está leyendo, o cuando se cierra y el usuario está viendo la tabla de contenido. Para proteger a los usuarios quiten un mensaje sin darse cuenta, MAPI define la eliminación de mensajes como un proceso de dos pasos:
  
1. Marcar un mensaje para su eliminación al mover a la carpeta que se ha designado como la carpeta Elementos eliminados: la carpeta cuyo identificador de entrada se almacena en la propiedad **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)). 
    
2. Quitar el mensaje llamando al método [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) . 
    
Cuando un usuario elige eliminar un mensaje en una carpeta distinta de la carpeta Elementos eliminados, marca para su eliminación. Sólo cuando un usuario selecciona mensajes desde la carpeta Elementos eliminados deben los mensajes físicamente quitarse de la estación de trabajo. Puede pedir al usuario que compruebe que el usuario realmente pensado para llevar a cabo la eliminación.
  
 **Para eliminar un mensaje**
  
1. Confirmar con el usuario que la eliminación inminente es intencionada.
    
2. Determinar el elemento principal de la carpeta que se va a eliminar. Si es la carpeta Elementos eliminados o en una subcarpeta dentro de la carpeta Elementos eliminados, llame a [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) para quitar el mensaje. 
    
3. Si la carpeta no se encuentra dentro de la carpeta Elementos eliminados, llame a [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) con el indicador MESSAGE_MOVE establecido para reubicar el mensaje a la carpeta Elementos eliminados. 
    

