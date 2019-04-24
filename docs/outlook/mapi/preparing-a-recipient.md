---
title: Preparación de un destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350676"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="9ee9d-103">Preparación de un destinatario</span><span class="sxs-lookup"><span data-stu-id="9ee9d-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="9ee9d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ee9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ee9d-105">Una aplicación cliente prepara a los destinatarios convirtiendo sus identificadores de entrada a corto plazo en identificadores de entrada a largo plazo y posiblemente agregando, cambiando o reordenando propiedades.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="9ee9d-106">Puede preparar a los destinatarios que forman parte de una lista de destinatarios para un mensaje o destinatarios que no están relacionados con un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="9ee9d-107">Normalmente, los clientes llaman a [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) directamente para convertir los identificadores de entrada a corto plazo en identificadores de entrada a largo plazo para los destinatarios que se incluyen en el cuadro de diálogo Dirección común.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="9ee9d-108">Para los destinatarios asociados a un mensaje saliente, la preparación del destinatario se controla mediante el proceso de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="9ee9d-109">Para preparar una lista de destinatarios, llame a **IAddrBook::P reparerecips**.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="9ee9d-110">**PrepareRecips** acepta una estructura [ADRLIST](adrlist.md) y una lista de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="9ee9d-111">La estructura **ADRLIST** contiene los destinatarios que se van a preparar, mientras que la lista de etiquetas de propiedades representa las propiedades que debe admitir cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="9ee9d-112">**PrepareRecips** intenta situar las propiedades que se incluyen en la lista de etiquetas de propiedad al principio de la estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="9ee9d-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="9ee9d-113">Si alguna de las propiedades de la lista falta en la estructura **ADRLIST** , MAPI llama al proveedor de la libreta de direcciones para proporcionarlas.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="9ee9d-114">Si solo necesita comprobar los identificadores de entrada a largo plazo, pase NULL para el parámetro _lpSPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="9ee9d-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="9ee9d-115">Por ejemplo, supongamos que está trabajando con cinco destinatarios.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="9ee9d-116">Los cinco destinatarios aparecen en la estructura **ADRLIST** con las propiedades siguientes en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee9d-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="9ee9d-117">\*\*\*\* Es ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ee9d-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="9ee9d-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ee9d-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="9ee9d-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ee9d-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="9ee9d-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ee9d-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="9ee9d-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ee9d-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="9ee9d-122">Se incluyen otras tres propiedades en la estructura **ADRLIST** para los dos primeros destinatarios.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="9ee9d-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ee9d-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="9ee9d-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ee9d-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="9ee9d-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ee9d-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="9ee9d-126">Como es necesario que todos los destinatarios tengan las tres primeras propiedades **PR_ADDRTYPE**, **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), cree una matriz de etiquetas de propiedad con estas propiedades y pase \*\*\*\* y la estructura **ADRLIST** a **PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="9ee9d-127">**PrepareRecips** llama al método **IMAPIProp:: GetProps** de cada destinatario para recuperar **PR_HOME_TELEPHONE_NUMBER** porque no forma parte actualmente de la estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="9ee9d-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="9ee9d-128">Cuando **PrepareRecips** devuelve, la lista de destinatarios representa una lista combinada de destinatarios con las propiedades incluidas en la estructura **ADRLIST** que aparecen primero para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="9ee9d-129">La lista de destinatarios de los destinatarios 1 y 2 incluye propiedades en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee9d-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="9ee9d-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="9ee9d-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="9ee9d-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="9ee9d-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="9ee9d-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="9ee9d-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="9ee9d-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="9ee9d-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="9ee9d-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="9ee9d-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="9ee9d-140">La lista de destinatarios para los destinatarios 3, 4 y 5 incluye propiedades en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ee9d-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="9ee9d-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="9ee9d-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="9ee9d-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="9ee9d-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="9ee9d-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="9ee9d-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="9ee9d-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="9ee9d-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="9ee9d-148">Como alternativa a llamar a **IAddrBook::P reparerecips** para trabajar con propiedades, llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) de cada uno de los destinatarios y, si es necesario, su método [IMAPIProp:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="9ee9d-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="9ee9d-149">Cuando sólo interviene un destinatario, cualquier técnica es satisfactoria.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="9ee9d-150">Sin embargo, cuando hay varios destinatarios implicados, llamar a **PrepareRecips** en lugar de a los métodos **IMAPIProp** ahorra tiempo y, si está operando de forma remota, a muchas llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="9ee9d-151">**PrepareRecips** procesa todos los destinatarios en una sola llamada mientras que **GetProps** y **SetProps** realizan una llamada para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="9ee9d-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

