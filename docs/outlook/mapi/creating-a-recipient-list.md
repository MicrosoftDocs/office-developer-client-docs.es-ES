---
title: Crear una lista de destinatarios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6de805da2aadd8ac40ca984c5f336d5ca7906248
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590130"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="f47f3-103">Crear una lista de destinatarios</span><span class="sxs-lookup"><span data-stu-id="f47f3-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="f47f3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f47f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f47f3-105">Una lista de destinatarios es una estructura [ADRLIST](adrlist.md) que contiene una matriz de estructuras de valor de propiedad para cada destinatario de mensaje: destino para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f47f3-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="f47f3-106">Un destinatario puede representar un usuario humano, un equipo o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f47f3-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="f47f3-107">Todos los mensajes que se envíen requieren al menos un destinatario que ha sido a través del proceso de resolución de nombre: un proceso para asegurarse de que la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) se incluye en la matriz de valores de propiedad del destinatario.</span><span class="sxs-lookup"><span data-stu-id="f47f3-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="f47f3-108">Las propiedades de un destinatario son una combinación de las propiedades de la libreta de direcciones y propiedades del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f47f3-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="f47f3-109">Propiedades del destinatario se pueden aplicar a todos los mensajes de un destinatario determinado o solo para el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="f47f3-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="f47f3-110">Ambos almacén de mensajes y los proveedores de transporte pueden establecer las propiedades de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f47f3-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="f47f3-111">Cada destinatario debe tener un conjunto básico de propiedades en su matriz de valores de propiedad en el momento en que el mensaje está listo para ser enviado.</span><span class="sxs-lookup"><span data-stu-id="f47f3-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="f47f3-112">El conjunto de propiedades del destinatario requerido incluyen:</span><span class="sxs-lookup"><span data-stu-id="f47f3-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="f47f3-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f47f3-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f47f3-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f47f3-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f47f3-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f47f3-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f47f3-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="f47f3-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="f47f3-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f47f3-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f47f3-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f47f3-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="f47f3-119">Estas propiedades se usan para tener acceso a los destinatarios, enviar mensajes a ella y para comparar a otras personas.</span><span class="sxs-lookup"><span data-stu-id="f47f3-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="f47f3-120">No todas estas propiedades deben estar disponibles inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f47f3-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="f47f3-121">Puede agregar a un destinatario inicialmente sin necesidad de conocer su identificador de entrada, confiar en el proceso de resolución de nombres para asignar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f47f3-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="f47f3-122">En algún momento antes de enviar un mensaje, llame a [IAddrBook::ResolveName](iaddrbook-resolvename.md) para asegurarse de que se resuelvan todos los destinatarios en la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f47f3-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="f47f3-123">Para obtener más información, vea la [resolución de un nombre del destinatario](resolving-a-recipient-name.md).</span><span class="sxs-lookup"><span data-stu-id="f47f3-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="f47f3-124">Las listas de destinatarios se pueden crear de mensajería a los usuarios o las entradas de la lista de distribución en un contenedor de la libreta de direcciones o de uso único.</span><span class="sxs-lookup"><span data-stu-id="f47f3-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="f47f3-125">Uso único es los destinatarios que se crean como entradas temporales para usarse sólo para hacer frente a un solo mensaje o como entradas que se agregarán a una libreta de direcciones personales.</span><span class="sxs-lookup"><span data-stu-id="f47f3-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="f47f3-126">El formato de un identificador de entrada con definición y una dirección se define mediante MAPI.</span><span class="sxs-lookup"><span data-stu-id="f47f3-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="f47f3-127">Para obtener más información acerca de estos formatos, consulte [Direcciones de uso único](one-off-addresses.md) y los [Identificadores de entrada de uso único](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="f47f3-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="f47f3-128">Puede habilitar a los usuarios crear sus listas de destinatarios:</span><span class="sxs-lookup"><span data-stu-id="f47f3-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="f47f3-129">Sólo con las entradas de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f47f3-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="f47f3-130">Sólo con las entradas de uso único.</span><span class="sxs-lookup"><span data-stu-id="f47f3-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="f47f3-131">Con una combinación de los destinatarios de la libreta de direcciones y de uso único.</span><span class="sxs-lookup"><span data-stu-id="f47f3-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="f47f3-132">**Para crear una lista de destinatarios mediante el cuadro de diálogo dirección comunes**</span><span class="sxs-lookup"><span data-stu-id="f47f3-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="f47f3-133">Asignar una estructura [ADRPARM](adrparm.md) y un puntero a una estructura [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="f47f3-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="f47f3-134">La memoria de la estructura de **ADRPARM** de cero y establecer el puntero **ADRLIST** en NULL.</span><span class="sxs-lookup"><span data-stu-id="f47f3-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="f47f3-135">Llame a [IAddrBook::Address](iaddrbook-address.md) para mostrar el cuadro de diálogo dirección y rellenar la estructura **ADRPARM** .</span><span class="sxs-lookup"><span data-stu-id="f47f3-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="f47f3-136">Llame a [IMessage::ModifyRecipients](imessage-modifyrecipients.md), pasando el puntero **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="f47f3-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="f47f3-137">Esta estructura contiene las propiedades de cada uno de los destinatarios seleccionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f47f3-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="f47f3-138">**Para crear una lista de destinatarios mediante programación**</span><span class="sxs-lookup"><span data-stu-id="f47f3-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="f47f3-139">Asignar una estructura **ADRLIST** que contiene una estructura [ADRENTRY](adrentry.md) para cada uno de los destinatarios que se deben incluir en la lista.</span><span class="sxs-lookup"><span data-stu-id="f47f3-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="f47f3-140">Hacer que cada estructura **ADRENTRY** suficientemente grande para contener cada una de las propiedades necesarias y **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f47f3-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="f47f3-141">Para cada destinatario, establezca la matriz de valores de propiedad para su miembro **aEntries** de la estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="f47f3-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="f47f3-142">Llame al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) con el conjunto de marca MODRECIP_ADD.</span><span class="sxs-lookup"><span data-stu-id="f47f3-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

