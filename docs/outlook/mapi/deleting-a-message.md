---
title: Eliminación de un mensaje
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
# <a name="deleting-a-message"></a>Eliminación de un mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un cliente puede eliminar un mensaje cuando está abierto y el usuario lo está leyendo, o cuando está cerrado y el usuario está viendo la tabla de contenido. Para proteger a un usuario de la eliminación accidental de un mensaje, MAPI define la eliminación de mensajes como un proceso de dos pasos:
  
1. Para marcar un mensaje para su eliminación, muévalo a la carpeta que se ha designado como carpeta elementos eliminados: la carpeta cuyo identificador de entrada se almacena en la propiedad **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)). 
    
2. Quite el mensaje mediante una llamada al método [IMAPIFolder::D eletemessages](imapifolder-deletemessages.md) . 
    
Cuando un usuario elige eliminar un mensaje en una carpeta distinta de la carpeta elementos eliminados, márquelo para su eliminación. Solo cuando un usuario selecciona mensajes desde dentro de la carpeta elementos eliminados, deben quitarse físicamente los mensajes de la estación de trabajo. Puede solicitar al usuario que compruebe que el usuario realmente está destinado a realizar la eliminación.
  
 **Para eliminar un mensaje**
  
1. Confirme con el usuario que la eliminación inminente es intencionada.
    
2. DeTermine el elemento primario de la carpeta que se va a eliminar. Si se trata de la carpeta elementos eliminados o una subcarpeta de la carpeta elementos eliminados, llame a [IMAPIFolder::D eletemessages](imapifolder-deletemessages.md) para quitar el mensaje. 
    
3. Si la carpeta no está contenida en la carpeta elementos eliminados, llame a [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) con la marca MESSAGE_MOVE establecida para reubicar el mensaje en la carpeta elementos eliminados. 
    

