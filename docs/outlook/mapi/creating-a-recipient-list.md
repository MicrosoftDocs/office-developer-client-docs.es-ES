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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332910"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="4fc2c-103">Creación de una lista de destinatarios</span><span class="sxs-lookup"><span data-stu-id="4fc2c-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="4fc2c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fc2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fc2c-105">Una lista de destinatarios es una estructura [ADRLIST](adrlist.md) que contiene una matriz de estructuras de valores de propiedad para cada destinatario de mensaje: destino del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="4fc2c-106">Un destinatario puede representar un usuario humano, un equipo o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="4fc2c-107">Todos los mensajes que se van a enviar requieren al menos un destinatario que ha recibido el proceso de resolución de nombres, es decir \*\*\*\* , un proceso para asegurarse de que la propiedad de ([PidTagEntryId](pidtagentryid-canonical-property.md)) se incluye en la matriz de valores de propiedad del destinatario.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="4fc2c-108">Las propiedades de un destinatario son una combinación de propiedades de la libreta de direcciones y propiedades del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="4fc2c-109">Las propiedades de los destinatarios se pueden aplicar a todos los mensajes de un destinatario en particular o solo al mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="4fc2c-110">Tanto el almacén de mensajes como los proveedores de transporte pueden establecer las propiedades de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="4fc2c-111">Cada destinatario debe tener un conjunto principal de propiedades en su matriz de valores de propiedad en el momento en que el mensaje esté listo para enviarse.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="4fc2c-112">El conjunto necesario de propiedades de destinatarios incluye:</span><span class="sxs-lookup"><span data-stu-id="4fc2c-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="4fc2c-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4fc2c-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="4fc2c-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4fc2c-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="4fc2c-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4fc2c-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="4fc2c-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="4fc2c-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="4fc2c-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4fc2c-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="4fc2c-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4fc2c-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="4fc2c-119">Estas propiedades se usan para tener acceso al destinatario, enviarle mensajes y compararlo con otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="4fc2c-120">No todas estas propiedades deben estar disponibles de inmediato.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="4fc2c-121">Puede Agregar un destinatario inicialmente sin conocer su identificador de entrada, sino que depende del proceso de resolución de nombres para asignar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="4fc2c-122">En algún momento antes de enviar un mensaje, llame a [IAddrBook:: ResolveName](iaddrbook-resolvename.md) para asegurarse de que se resuelven todos los destinatarios de la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="4fc2c-123">Para obtener más información, vea [resolver un nombre de destinatario](resolving-a-recipient-name.md).</span><span class="sxs-lookup"><span data-stu-id="4fc2c-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="4fc2c-124">Las listas de destinatarios se pueden crear a partir de usuarios de mensajería o entradas de listas de distribución en un contenedor de libretas de direcciones o de desventajas.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="4fc2c-125">Las cancelaciones son destinatarios que se crean como entradas temporales para usarse solo para enviar un solo mensaje o como entradas que se agregarán a la libreta personal de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="4fc2c-126">MAPI define el formato de una dirección y un identificador de entrada de un solo uso.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="4fc2c-127">Para obtener más información sobre estos formatos, vea [direcciones de un solo uso](one-off-addresses.md) y [identificadores de entrada de un solo uso](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="4fc2c-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="4fc2c-128">Puede permitir que los usuarios creen sus listas de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="4fc2c-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="4fc2c-129">Solo con entradas de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="4fc2c-130">Solo con las entradas de uso único.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="4fc2c-131">Con una combinación de destinatarios de la libreta de direcciones y una sola desventajas.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="4fc2c-132">**Para crear una lista de destinatarios mediante el cuadro de diálogo Dirección común**</span><span class="sxs-lookup"><span data-stu-id="4fc2c-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="4fc2c-133">Asigne una estructura [ADRPARM](adrparm.md) y un puntero a una estructura [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="4fc2c-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="4fc2c-134">Cero la memoria de la estructura **ADRPARM** y el puntero **ADRLIST** se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="4fc2c-135">Llame a [IAddrBook:: Address](iaddrbook-address.md) para mostrar el cuadro de diálogo address y rellenar la estructura **ADRPARM** .</span><span class="sxs-lookup"><span data-stu-id="4fc2c-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="4fc2c-136">Llame a [IMessage:: ModifyRecipients](imessage-modifyrecipients.md), pasando el puntero **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="4fc2c-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="4fc2c-137">Esta estructura contendrá las propiedades de cada uno de los destinatarios seleccionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="4fc2c-138">**Para crear una lista de destinatarios mediante programación**</span><span class="sxs-lookup"><span data-stu-id="4fc2c-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="4fc2c-139">Asigne una estructura **ADRLIST** que contenga una estructura [ADRENTRY](adrentry.md) para cada uno de los destinatarios que se incluirán en la lista.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="4fc2c-140">Haga que cada estructura **ADRENTRY** sea lo suficientemente grande como para guardar cada una de las propiedades y **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) necesarias.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="4fc2c-141">Para cada destinatario, establezca la matriz de valores de propiedad para su miembro **aEntries** en la estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="4fc2c-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="4fc2c-142">Llame a [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) con la marca MODRECIP_ADD establecida.</span><span class="sxs-lookup"><span data-stu-id="4fc2c-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

