---
title: Tablas de destinatarios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: cc7635c474b99898d59589f33fcf06cf24697378
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820476"
---
# <a name="recipient-tables"></a><span data-ttu-id="1d823-103">Tablas de destinatarios</span><span class="sxs-lookup"><span data-stu-id="1d823-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="1d823-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1d823-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1d823-105">La tabla de destinatarios contiene información acerca de todos los destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1d823-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="1d823-106">Los proveedores de almacén de mensajes implementan tablas de destinatarios y usan en las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="1d823-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="1d823-107">Los clientes de acceso a una tabla de destinatario mediante la realización de una llamada al método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) , o si el mensaje de proveedor de almacén lo admite, al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="1d823-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="1d823-108">Los clientes de tener acceso a tablas de destinatarios con **OpenProperty** mediante la especificación de **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) para la etiqueta de propiedad y IID_IMAPITable para el identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="1d823-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="1d823-109">Los cambios realizados en una tabla de destinatario pueden estar llamando al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="1d823-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="1d823-110">Tablas de destinatarios tienen una columna diferente establecer dependiendo de si se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="1d823-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="1d823-111">Las siguientes propiedades que conforman la columna requiere establecer en tablas de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="1d823-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="1d823-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d823-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="1d823-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d823-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="1d823-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d823-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="1d823-115">Las propiedades opcionales son:</span><span class="sxs-lookup"><span data-stu-id="1d823-115">The optional properties are:</span></span>
  
- <span data-ttu-id="1d823-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d823-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="1d823-117">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d823-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="1d823-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d823-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="1d823-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d823-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="1d823-120">Los mensajes enviados deben incluir estas propiedades adicionales en su conjunto de columna necesarios:</span><span class="sxs-lookup"><span data-stu-id="1d823-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="1d823-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d823-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="1d823-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d823-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="1d823-123">Dependiendo de la implementación de un proveedor, es posible columnas adicionales, como **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) y la [propiedad ENTRYID](entryid.md), en la tabla.</span><span class="sxs-lookup"><span data-stu-id="1d823-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="1d823-124">Cualquier proveedor de almacén de mensajes que admite la transmisión de mensajes, indicada por el bit STORE_SUBMIT_OK que se establece en la propiedad del proveedor **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), debe ofrecer compatibilidad con un conjunto determinado de restricciones en una implementación de la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="1d823-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="1d823-125">Existe el **y**, **o**, y restricciones de propiedad están entre los tipos de restricciones que deberían estar disponibles para los usuarios de la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="1d823-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="1d823-126">Sólo los operadores iguales y no es iguales que necesite ser compatible con la restricción de propiedad.</span><span class="sxs-lookup"><span data-stu-id="1d823-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="1d823-127">Estas restricciones deben trabajar con las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="1d823-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="1d823-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="1d823-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="1d823-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d823-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="1d823-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="1d823-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="1d823-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="1d823-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="1d823-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="1d823-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d823-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="1d823-133">See also</span></span>



[<span data-ttu-id="1d823-134">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="1d823-134">MAPI Tables</span></span>](mapi-tables.md)

