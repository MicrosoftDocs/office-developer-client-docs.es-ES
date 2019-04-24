---
title: Tablas de destinatarios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328423"
---
# <a name="recipient-tables"></a><span data-ttu-id="bce80-103">Tablas de destinatarios</span><span class="sxs-lookup"><span data-stu-id="bce80-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="bce80-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bce80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bce80-105">La tabla recipient contiene información sobre todos los destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="bce80-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="bce80-106">Los proveedores de almacenamiento de mensajes implementan tablas de destinatarios y las aplicaciones cliente las usan.</span><span class="sxs-lookup"><span data-stu-id="bce80-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="bce80-107">Los clientes tienen acceso a una tabla de destinatarios realizando una llamada al método [IMessage:: GetRecipientTable](imessage-getrecipienttable.md) o, si el proveedor de almacenamiento de mensajes lo admite, al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="bce80-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="bce80-108">Los clientes tienen acceso a las tablas de destinatarios con **OpenProperty** especificando **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) para la etiqueta de propiedad y IID_IMAPITable para el identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="bce80-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="bce80-109">Los cambios en una tabla de destinatarios pueden realizarse llamando al método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="bce80-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="bce80-110">Las tablas de destinatarios tienen un conjunto de columnas diferente en función de si se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="bce80-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="bce80-111">Las siguientes propiedades componen el conjunto de columnas necesario en las tablas de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="bce80-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="bce80-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bce80-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="bce80-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bce80-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="bce80-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bce80-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="bce80-115">Las propiedades opcionales son:</span><span class="sxs-lookup"><span data-stu-id="bce80-115">The optional properties are:</span></span>
  
- <span data-ttu-id="bce80-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bce80-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="bce80-117">\*\*\*\* Es ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bce80-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="bce80-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bce80-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="bce80-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bce80-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="bce80-120">Los mensajes enviados deben incluir estas propiedades adicionales en el conjunto de columnas necesario:</span><span class="sxs-lookup"><span data-stu-id="bce80-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="bce80-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bce80-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="bce80-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bce80-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="bce80-123">En función de la implementación de un proveedor, las columnas adicionales, como **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) y [EntryID](entryid.md), podrían estar en la tabla.</span><span class="sxs-lookup"><span data-stu-id="bce80-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="bce80-124">Cualquier proveedor de almacenamiento de mensajes que admita la transmisión de mensajes, como indica el bit STORE_SUBMIT_OK que se establece en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del proveedor, debe ofrecer compatibilidad con un conjunto determinado de restricciones en una implementación de tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="bce80-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="bce80-125">Las restricciones **and**, **or**, exist y Property se encuentran entre los tipos de restricciones que deben estar disponibles para los usuarios de la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="bce80-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="bce80-126">Sólo los operadores igual y no igual deben ser compatibles con la restricción de propiedad.</span><span class="sxs-lookup"><span data-stu-id="bce80-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="bce80-127">Estas restricciones deben funcionar con las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="bce80-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="bce80-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="bce80-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="bce80-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bce80-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="bce80-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="bce80-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="bce80-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="bce80-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="bce80-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="bce80-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bce80-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="bce80-133">See also</span></span>



[<span data-ttu-id="bce80-134">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="bce80-134">MAPI Tables</span></span>](mapi-tables.md)

