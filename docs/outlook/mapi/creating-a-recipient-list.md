---
title: Creación de una lista de destinatarios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e3aa1f2b2e1e7c6d8a9be3fff451002952930ffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428217"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="0956b-103">Creación de una lista de destinatarios</span><span class="sxs-lookup"><span data-stu-id="0956b-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="0956b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0956b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0956b-105">Una lista de destinatarios es una [estructura ADRLIST](adrlist.md) que contiene una matriz de estructuras de valores de propiedad para cada destinatario de mensaje: destino del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0956b-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="0956b-106">Un destinatario puede representar un usuario humano, una máquina o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="0956b-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="0956b-107">Todos los mensajes que se enviarán requieren al menos un destinatario que haya pasado por el proceso de resolución de nombres, un proceso para garantizar que la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) se incluya en la matriz de valores de propiedad del destinatario.</span><span class="sxs-lookup"><span data-stu-id="0956b-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="0956b-108">Las propiedades de un destinatario son una combinación de propiedades de libreta de direcciones y propiedades de mensaje.</span><span class="sxs-lookup"><span data-stu-id="0956b-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="0956b-109">Las propiedades de destinatario pueden aplicarse a todos los mensajes de un destinatario determinado o solo al mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="0956b-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="0956b-110">Tanto el almacén de mensajes como los proveedores de transporte pueden establecer propiedades de destinatario.</span><span class="sxs-lookup"><span data-stu-id="0956b-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="0956b-111">Cada destinatario debe tener un conjunto principal de propiedades en su matriz de valores de propiedad cuando el mensaje esté listo para enviarse.</span><span class="sxs-lookup"><span data-stu-id="0956b-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="0956b-112">El conjunto necesario de propiedades de destinatario incluyen:</span><span class="sxs-lookup"><span data-stu-id="0956b-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="0956b-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0956b-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="0956b-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0956b-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="0956b-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0956b-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="0956b-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="0956b-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="0956b-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0956b-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="0956b-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0956b-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="0956b-119">Estas propiedades se usan para obtener acceso al destinatario, enviarle mensajes y compararlo con otros.</span><span class="sxs-lookup"><span data-stu-id="0956b-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="0956b-120">No todas estas propiedades deben estar disponibles inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="0956b-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="0956b-121">Puede agregar un destinatario inicialmente sin conocer su identificador de entrada, basándose en el proceso de resolución de nombres para asignar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0956b-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="0956b-122">En algún momento antes de enviar un mensaje, llama a [IAddrBook::ResolveName](iaddrbook-resolvename.md) para asegurarte de que se resuelvan todos los destinatarios de la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="0956b-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="0956b-123">Para obtener más información, vea [Resolving a Recipient Name](resolving-a-recipient-name.md).</span><span class="sxs-lookup"><span data-stu-id="0956b-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="0956b-124">Las listas de destinatarios se pueden crear a partir de usuarios de mensajería o entradas de listas de distribución en un contenedor de libreta de direcciones o desde uno solo.</span><span class="sxs-lookup"><span data-stu-id="0956b-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="0956b-125">Los one-offs son destinatarios que se crean como entradas temporales que se usan solo para dirigir un único mensaje o como entradas que se van a agregar a una libreta de direcciones personal.</span><span class="sxs-lookup"><span data-stu-id="0956b-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="0956b-126">MAPI define el formato de un identificador de entrada y una dirección únicos.</span><span class="sxs-lookup"><span data-stu-id="0956b-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="0956b-127">Para obtener más información acerca de estos [formatos,](one-off-entry-identifiers.md)vea Direcciones de un solo [uso](one-off-addresses.md) e Identificadores de entrada de un solo uso .</span><span class="sxs-lookup"><span data-stu-id="0956b-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="0956b-128">Puede permitir a los usuarios crear sus listas de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="0956b-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="0956b-129">Solo con entradas de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="0956b-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="0956b-130">Solo con entradas únicas.</span><span class="sxs-lookup"><span data-stu-id="0956b-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="0956b-131">Con una combinación de destinatarios de libreta de direcciones y one-offs.</span><span class="sxs-lookup"><span data-stu-id="0956b-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="0956b-132">**Para crear una lista de destinatarios mediante el cuadro de diálogo dirección común**</span><span class="sxs-lookup"><span data-stu-id="0956b-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="0956b-133">Asigne una [estructura ADRPARM](adrparm.md) y un puntero a una [estructura ADRLIST.](adrlist.md)</span><span class="sxs-lookup"><span data-stu-id="0956b-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="0956b-134">Cero la memoria en la **estructura ADRPARM** y establezca el **puntero ADRLIST** en NULL.</span><span class="sxs-lookup"><span data-stu-id="0956b-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="0956b-135">Llama [a IAddrBook::Address](iaddrbook-address.md) para mostrar el cuadro de diálogo dirección y rellenar la **estructura ADRPARM.**</span><span class="sxs-lookup"><span data-stu-id="0956b-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="0956b-136">Llama [a IMessage::ModifyRecipients](imessage-modifyrecipients.md)y pasa el **puntero ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="0956b-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="0956b-137">Esta estructura contendrá las propiedades de cada uno de los destinatarios seleccionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0956b-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="0956b-138">**Para crear una lista de destinatarios mediante programación**</span><span class="sxs-lookup"><span data-stu-id="0956b-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="0956b-139">Asigne una **estructura ADRLIST** que contenga una [estructura ADRENTRY](adrentry.md) para cada uno de los destinatarios que se incluirán en la lista.</span><span class="sxs-lookup"><span data-stu-id="0956b-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="0956b-140">Haga que **cada estructura ADRENTRY** sea lo suficientemente grande como para contener cada una de las propiedades necesarias **y PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0956b-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="0956b-141">Para cada destinatario, establezca la matriz de valores de propiedad para su **miembro aEntries** en la **estructura ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="0956b-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="0956b-142">Llama [a IMessage::ModifyRecipients](imessage-modifyrecipients.md) con el MODRECIP_ADD marca establecida.</span><span class="sxs-lookup"><span data-stu-id="0956b-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

