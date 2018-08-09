---
title: Preparar un destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 51241009262471bf30f7d71e3108b896bbce8df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820437"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="89404-103">Preparar un destinatario</span><span class="sxs-lookup"><span data-stu-id="89404-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="89404-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="89404-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="89404-105">Una aplicación cliente prepara a los destinatarios mediante la conversión de sus identificadores de entrada a corto plazo a los identificadores de entrada a largo plazo y, posiblemente, agregar, cambiar o reordenación de propiedades.</span><span class="sxs-lookup"><span data-stu-id="89404-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="89404-106">Puede preparar los destinatarios que forman parte de una lista de destinatarios para un mensaje o los destinatarios que no están relacionados con un mensaje.</span><span class="sxs-lookup"><span data-stu-id="89404-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="89404-107">Normalmente, los clientes llaman [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directamente para convertir los identificadores de entrada a corto plazo en los identificadores de entrada a largo plazo para los destinatarios que se incluyen en el cuadro de diálogo dirección comunes.</span><span class="sxs-lookup"><span data-stu-id="89404-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="89404-108">Para los destinatarios que están asociados con un mensaje saliente, la preparación del destinatario se administra mediante el proceso de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="89404-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="89404-109">Para preparar una lista de destinatarios, llame a **IAddrBook::PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="89404-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="89404-110">**PrepareRecips** acepta una estructura de [ADRLIST](adrlist.md) y una lista de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="89404-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="89404-111">La estructura **ADRLIST** contiene los destinatarios para estar preparado mientras la lista de etiquetas de propiedad representa las propiedades que debe admitir cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="89404-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="89404-112">**PrepareRecips** intenta colocar las propiedades que se incluyen en la lista de etiquetas de propiedad al principio de la estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="89404-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="89404-113">Si cualquiera de las propiedades en la lista faltan de la estructura **ADRLIST** , MAPI llama al proveedor de la libreta de direcciones para proporcionar ellos.</span><span class="sxs-lookup"><span data-stu-id="89404-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="89404-114">Si sólo necesita comprobar si los identificadores de entrada a largo plazo, pase NULL para el parámetro _lpSPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="89404-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="89404-115">Por ejemplo, suponga que trabaja con cinco destinatarios.</span><span class="sxs-lookup"><span data-stu-id="89404-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="89404-116">Todos los destinatarios de cinco aparecen en la estructura **ADRLIST** con las propiedades siguientes en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="89404-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="89404-117">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89404-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="89404-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89404-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="89404-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89404-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="89404-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89404-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="89404-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89404-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="89404-122">Otras tres propiedades se incluyen en la estructura **ADRLIST** para los dos primeros destinatarios.</span><span class="sxs-lookup"><span data-stu-id="89404-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="89404-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89404-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="89404-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89404-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="89404-125">**PR_SURNAME** ([Pidtagsurname MAPI](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89404-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="89404-126">Dado que todos los destinatarios necesitan tener como sus tres primeros propiedades **PR_ADDRTYPE**, **entrada del objeto**y **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), cree una matriz de etiqueta de propiedad con estas propiedades y pase se y la estructura **ADRLIST** a **PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="89404-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="89404-127">**PrepareRecips** llama al método **IMAPIProp::GetProps** de cada destinatario para recuperar **PR_HOME_TELEPHONE_NUMBER** debido a que actualmente no es parte de la estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="89404-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="89404-128">Cuando se devuelve **PrepareRecips** , la lista de destinatarios representa una lista combinada de los destinatarios con las propiedades incluidas en la estructura **ADRLIST** que aparezcan en primer lugar para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="89404-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="89404-129">La lista de destinatarios para los destinatarios 1 y 2 incluye propiedades en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="89404-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="89404-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="89404-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="89404-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="89404-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="89404-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="89404-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="89404-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="89404-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="89404-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="89404-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="89404-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="89404-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="89404-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="89404-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="89404-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="89404-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="89404-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="89404-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="89404-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="89404-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="89404-140">La lista de destinatarios para los destinatarios 3, 4 y 5 incluye propiedades en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="89404-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="89404-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="89404-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="89404-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="89404-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="89404-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="89404-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="89404-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="89404-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="89404-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="89404-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="89404-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="89404-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="89404-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="89404-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="89404-148">Como alternativa a llamar al método **IAddrBook::PrepareRecips** para trabajar con las propiedades, llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) de cada destinatario y, si es necesario, su método [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="89404-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="89404-149">Cuando un solo destinatario está implicado, cualquiera de estas técnicas sea satisfactoria.</span><span class="sxs-lookup"><span data-stu-id="89404-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="89404-150">Sin embargo, cuando son necesarios para varios destinatarios, al llamar a **PrepareRecips** en lugar de los métodos de **IMAPIProp** ahorra tiempo y, si está trabajando de forma remota, todas las llamadas a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="89404-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="89404-151">**PrepareRecips** procesa a todos los destinatarios en una sola llamada mientras que **GetProps** y **SetProps** realizar una llamada para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="89404-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

