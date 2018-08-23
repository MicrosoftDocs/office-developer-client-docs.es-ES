---
title: Direcciones SMTP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 655d48d1ea937659f85e0ef7379425759ea7e256
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591362"
---
# <a name="smtp-addresses"></a><span data-ttu-id="e71bc-103">Direcciones SMTP</span><span class="sxs-lookup"><span data-stu-id="e71bc-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="e71bc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e71bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e71bc-105">El formato de direcciones de correo electrónico de SMTP se define en RFC 822.</span><span class="sxs-lookup"><span data-stu-id="e71bc-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="e71bc-106">Componentes MAPI deben controlar todas las direcciones que cumplen con ese estándar.</span><span class="sxs-lookup"><span data-stu-id="e71bc-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="e71bc-107">Sin embargo, hay una forma especial de dirección RFC 822 que mejor se codifica las direcciones MAPI:</span><span class="sxs-lookup"><span data-stu-id="e71bc-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="e71bc-108">_nombre para mostrar_ **\<** _dirección de correo electrónico_**\>**</span><span class="sxs-lookup"><span data-stu-id="e71bc-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="e71bc-109">Los corchetes angulares se incluyen como literales.</span><span class="sxs-lookup"><span data-stu-id="e71bc-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="e71bc-110">Celdas en blanco son comunes en los nombres para mostrar; necesitan no ir entre comillas.</span><span class="sxs-lookup"><span data-stu-id="e71bc-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="e71bc-111">Una dirección típica podría ser como éste, que pertenece a uno de los coautores de RFC 1521:</span><span class="sxs-lookup"><span data-stu-id="e71bc-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="e71bc-112">Nathaniel Borenstein \<nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="e71bc-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="e71bc-113">Si el nombre para mostrar contiene caracteres que tienen un significado especial en las direcciones SMTP, como \< o @, el nombre para mostrar completo debe estar entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="e71bc-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="e71bc-114">En el correo saliente, si la longitud total de la dirección de correo electrónico y Mostrar nombre supera los 255 caracteres, se debe quitar el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e71bc-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="e71bc-115">Las partes de una dirección SMTP se asignarán a propiedades MAPI de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="e71bc-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="e71bc-116">**Componente de dirección SMTP**</span><span class="sxs-lookup"><span data-stu-id="e71bc-116">**SMTP address component**</span></span>|<span data-ttu-id="e71bc-117">**Propiedad MAPI**</span><span class="sxs-lookup"><span data-stu-id="e71bc-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e71bc-118">_nombre para mostrar_ para todos los destinatarios</span><span class="sxs-lookup"><span data-stu-id="e71bc-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="e71bc-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e71bc-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="e71bc-120">_nombre para mostrar_ para el campo</span><span class="sxs-lookup"><span data-stu-id="e71bc-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="e71bc-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e71bc-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="e71bc-122">_nombre para mostrar_ para el campo de remitente</span><span class="sxs-lookup"><span data-stu-id="e71bc-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="e71bc-123">**PR_SENT_REPRESENTING_NAME de MAPI** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e71bc-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="e71bc-124">_dirección de correo electrónico_</span><span class="sxs-lookup"><span data-stu-id="e71bc-124">_email-address_</span></span> <br/> |<span data-ttu-id="e71bc-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e71bc-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="e71bc-126">implícitas, siempre "SMTP"</span><span class="sxs-lookup"><span data-stu-id="e71bc-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="e71bc-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e71bc-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="e71bc-128">Si no hay ningún nombre para mostrar para una dirección de correo entrante, la dirección de correo electrónico completa debe usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e71bc-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="e71bc-129">El tipo de dirección siempre es SMTP.</span><span class="sxs-lookup"><span data-stu-id="e71bc-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="e71bc-130">Las propiedades de destinatarios se toman de la tabla de destinatarios del mensaje MAPI; propiedades de remitente se toman desde el propio mensaje.</span><span class="sxs-lookup"><span data-stu-id="e71bc-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

