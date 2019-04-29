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
ms.openlocfilehash: c5880aefe7c2dba2e5e4c5405aae2020bb86c711
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410052"
---
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="a4a96-103">attConversationID y attParentID</span><span class="sxs-lookup"><span data-stu-id="a4a96-103">attConversationID and attParentID</span></span>

<span data-ttu-id="a4a96-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4a96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4a96-105">La clave de la conversación de correo de Windows para trabajo en grupo 3,1 es una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="a4a96-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="a4a96-106">El equivalente de MAPI es un valor binario.</span><span class="sxs-lookup"><span data-stu-id="a4a96-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="a4a96-107">Para proporcionar compatibilidad con versiones anteriores, la implementación de TNEF convierte los datos binarios en texto y agrega un carácter null de terminación.</span><span class="sxs-lookup"><span data-stu-id="a4a96-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a4a96-108">Las propiedades correspondientes de MAPI a las que se asignan estos atributos TNEF, PR_CONVERSATION_KEY y PR_PARENT_KEY, han quedado en desuso en Microsoft Exchange Server: uso de **PR_CONVERSATION_KEY**, el [PidTagConversationKey canónico Propiedad](pidtagconversationkey-canonical-property.md), sólo se conserva en Outlook para buscar \*\*IPM. \*\*Mensajes de MessageManager.</span><span class="sxs-lookup"><span data-stu-id="a4a96-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a4a96-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4a96-109">Remarks</span></span>

<span data-ttu-id="a4a96-110">La propiedad **PR_CONVERSATION_KEY** es el precursor contrario obsoleto del **PR_CONVERSATION_INDEX**, la [propiedad canónica PidTagConversationIndex](pidtagconversationindex-canonical-property.md) y **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic canónico ](pidtagconversationtopic-canonical-property.md), Que se debe usar en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a4a96-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a4a96-111">Ver también</span><span class="sxs-lookup"><span data-stu-id="a4a96-111">See also</span></span>

- [<span data-ttu-id="a4a96-112">Subárbol IPM</span><span class="sxs-lookup"><span data-stu-id="a4a96-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="a4a96-113">Carpetas especiales de MAPI</span><span class="sxs-lookup"><span data-stu-id="a4a96-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

