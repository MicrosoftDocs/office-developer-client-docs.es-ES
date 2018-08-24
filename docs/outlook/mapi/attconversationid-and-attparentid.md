---
title: attConversationID y attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: 'Última modificación: 12 de marzo de 2013'
ms.openlocfilehash: 14b93a952e4776716c333dc730144b55bcc61259
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582717"
---
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="6197f-103">attConversationID y attParentID</span><span class="sxs-lookup"><span data-stu-id="6197f-103">attConversationID and attParentID</span></span>

<span data-ttu-id="6197f-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6197f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6197f-105">Las ventanas de clave de conversación de correo de trabajo en grupo 3.1 son una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="6197f-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="6197f-106">El equivalente MAPI es un valor binario.</span><span class="sxs-lookup"><span data-stu-id="6197f-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="6197f-107">Para proporcionar compatibilidad con versiones anteriores, la implementación de TNEF convierte los datos binarios en texto y agrega un carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="6197f-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6197f-108">Las propiedades correspondientes en MAPI para que se asignan estos atributos TNEF, PR_CONVERSATION_KEY y PR_PARENT_KEY, han quedado obsoletos en Microsoft Exchange Server: uso de **PR_CONVERSATION_KEY**, el [PidTagConversationKey canónico Propiedad](pidtagconversationkey-canonical-property.md), se conserva en Outlook sólo, para localizar **IPM. Objeto** los mensajes.</span><span class="sxs-lookup"><span data-stu-id="6197f-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6197f-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6197f-109">Remarks</span></span>

<span data-ttu-id="6197f-110">La propiedad **PR_CONVERSATION_KEY** es el precursor en caso contrario, obsoleto **PR_CONVERSATION_INDEX**, [Propiedad canónico PidTagConversationIndex](pidtagconversationindex-canonical-property.md) y **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic canónico Propiedad](pidtagconversationtopic-canonical-property.md), que se debe usar en su lugar.</span><span class="sxs-lookup"><span data-stu-id="6197f-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6197f-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="6197f-111">See also</span></span>

- [<span data-ttu-id="6197f-112">Subárbol IPM</span><span class="sxs-lookup"><span data-stu-id="6197f-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="6197f-113">Carpetas especiales de MAPI</span><span class="sxs-lookup"><span data-stu-id="6197f-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

