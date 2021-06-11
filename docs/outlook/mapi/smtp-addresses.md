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
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419628"
---
# <a name="smtp-addresses"></a><span data-ttu-id="970ee-103">Direcciones SMTP</span><span class="sxs-lookup"><span data-stu-id="970ee-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="970ee-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="970ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="970ee-105">El formato de las direcciones de correo electrónico SMTP se define en RFC 822.</span><span class="sxs-lookup"><span data-stu-id="970ee-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="970ee-106">Los componentes MAPI deben controlar cualquier dirección que cumpla con ese estándar.</span><span class="sxs-lookup"><span data-stu-id="970ee-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="970ee-107">Sin embargo, hay una forma particular de dirección RFC 822 que codifica mejor las direcciones MAPI:</span><span class="sxs-lookup"><span data-stu-id="970ee-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="970ee-108">_nombre para mostrar_ **\<** _email-address_**\>**</span><span class="sxs-lookup"><span data-stu-id="970ee-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="970ee-109">Los corchetes angulares se incluyen como literales.</span><span class="sxs-lookup"><span data-stu-id="970ee-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="970ee-110">Los espacios en blanco son comunes en los nombres para mostrar; no es necesario que se cite.</span><span class="sxs-lookup"><span data-stu-id="970ee-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="970ee-111">Una dirección típica podría tener este aspecto, que pertenece a uno de los coautores de RFC 1521:</span><span class="sxs-lookup"><span data-stu-id="970ee-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="970ee-112">Nathaniel Borenstein \< nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="970ee-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="970ee-113">Si el nombre para mostrar contiene caracteres que tienen un significado especial en las direcciones SMTP, como o @, todo el nombre para mostrar debe incluirse \< entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="970ee-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="970ee-114">En el correo saliente, si la longitud total de la dirección de correo electrónico más el nombre para mostrar supera los 255 caracteres, se debe descartar el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="970ee-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="970ee-115">Las partes de una dirección SMTP se asignan a las propiedades MAPI de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="970ee-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="970ee-116">**Componente de dirección SMTP**</span><span class="sxs-lookup"><span data-stu-id="970ee-116">**SMTP address component**</span></span>|<span data-ttu-id="970ee-117">**Mapi (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="970ee-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="970ee-118">_nombre para mostrar_ para todos los destinatarios</span><span class="sxs-lookup"><span data-stu-id="970ee-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="970ee-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="970ee-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="970ee-120">_nombre para mostrar_ para el campo De</span><span class="sxs-lookup"><span data-stu-id="970ee-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="970ee-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="970ee-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="970ee-122">_nombre para mostrar_ para el campo Remitente</span><span class="sxs-lookup"><span data-stu-id="970ee-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="970ee-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="970ee-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="970ee-124">_email-address_</span><span class="sxs-lookup"><span data-stu-id="970ee-124">_email-address_</span></span> <br/> |<span data-ttu-id="970ee-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="970ee-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="970ee-126">implícito, siempre "SMTP"</span><span class="sxs-lookup"><span data-stu-id="970ee-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="970ee-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="970ee-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="970ee-128">Si no hay ningún nombre para mostrar para una dirección en el correo entrante, se debe usar la dirección de correo electrónico completa en su lugar.</span><span class="sxs-lookup"><span data-stu-id="970ee-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="970ee-129">El tipo de dirección es siempre SMTP.</span><span class="sxs-lookup"><span data-stu-id="970ee-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="970ee-130">Las propiedades de destinatario se toman de la tabla de destinatarios del mensaje MAPI; las propiedades del remitente se toman del propio mensaje.</span><span class="sxs-lookup"><span data-stu-id="970ee-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

