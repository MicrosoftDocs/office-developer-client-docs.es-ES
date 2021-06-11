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
# <a name="deleting-a-message"></a><span data-ttu-id="b26b6-103">Eliminar un mensaje</span><span class="sxs-lookup"><span data-stu-id="b26b6-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="b26b6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b26b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b26b6-105">Un cliente puede eliminar un mensaje cuando está abierto y el usuario lo está leyendo, o cuando se cierra y el usuario está viendo la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="b26b6-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="b26b6-106">Para proteger a un usuario de la eliminación involuntaria de un mensaje, MAPI define la eliminación de mensajes como un proceso de dos pasos:</span><span class="sxs-lookup"><span data-stu-id="b26b6-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="b26b6-107">Marca un mensaje para eliminarlo moviéndolo a la carpeta designada como carpeta Elementos eliminados, la carpeta cuyo identificador de entrada se almacena en la propiedad **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b26b6-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="b26b6-108">Quite el mensaje llamando al [método IMAPIFolder::D eleteMessages.](imapifolder-deletemessages.md)</span><span class="sxs-lookup"><span data-stu-id="b26b6-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="b26b6-109">Cuando un usuario elija eliminar un mensaje en una carpeta que no sea la carpeta Elementos eliminados, marque para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="b26b6-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="b26b6-110">Solo cuando un usuario selecciona mensajes de la carpeta Elementos eliminados si los mensajes se quitan físicamente de la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="b26b6-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="b26b6-111">Puede solicitar al usuario que compruebe que el usuario realmente tiene la intención de realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="b26b6-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="b26b6-112">**Para eliminar un mensaje**</span><span class="sxs-lookup"><span data-stu-id="b26b6-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="b26b6-113">Confirme con el usuario que la eliminación inminente es intencionada.</span><span class="sxs-lookup"><span data-stu-id="b26b6-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="b26b6-114">Determine el elemento primario de la carpeta que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="b26b6-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="b26b6-115">Si es la carpeta Elementos eliminados o una subcarpeta de la carpeta Elementos eliminados, llame a [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md) para quitar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b26b6-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="b26b6-116">Si la carpeta no está incluida en la carpeta Elementos eliminados, llame a [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) con la marca MESSAGE_MOVE establecida para reubicar el mensaje en la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b26b6-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

