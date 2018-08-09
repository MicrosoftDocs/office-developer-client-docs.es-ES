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
ms.openlocfilehash: 9bc77e3226066dc88bbaf4f4efc324825add8919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820724"
---
# <a name="smtp-addresses"></a><span data-ttu-id="5a71f-103">Direcciones SMTP</span><span class="sxs-lookup"><span data-stu-id="5a71f-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="5a71f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a71f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a71f-105">El formato de direcciones de correo electrónico de SMTP se define en RFC 822.</span><span class="sxs-lookup"><span data-stu-id="5a71f-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="5a71f-106">Componentes MAPI deben controlar todas las direcciones que cumplen con ese estándar.</span><span class="sxs-lookup"><span data-stu-id="5a71f-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="5a71f-107">Sin embargo, hay una forma especial de dirección RFC 822 que mejor se codifica las direcciones MAPI:</span><span class="sxs-lookup"><span data-stu-id="5a71f-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="5a71f-108">_nombre para mostrar_ **\<** _dirección de correo electrónico_**\>**</span><span class="sxs-lookup"><span data-stu-id="5a71f-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="5a71f-109">Los corchetes angulares se incluyen como literales.</span><span class="sxs-lookup"><span data-stu-id="5a71f-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="5a71f-110">Celdas en blanco son comunes en los nombres para mostrar; necesitan no ir entre comillas.</span><span class="sxs-lookup"><span data-stu-id="5a71f-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="5a71f-111">Una dirección típica podría ser como éste, que pertenece a uno de los coautores de RFC 1521:</span><span class="sxs-lookup"><span data-stu-id="5a71f-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="5a71f-112">Nathaniel Borenstein \<nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="5a71f-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="5a71f-113">Si el nombre para mostrar contiene caracteres que tienen un significado especial en las direcciones SMTP, como \< o @, el nombre para mostrar completo debe estar entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="5a71f-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="5a71f-114">En el correo saliente, si la longitud total de la dirección de correo electrónico y Mostrar nombre supera los 255 caracteres, se debe quitar el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="5a71f-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="5a71f-115">Las partes de una dirección SMTP se asignarán a propiedades MAPI de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5a71f-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="5a71f-116">**Componente de dirección SMTP**</span><span class="sxs-lookup"><span data-stu-id="5a71f-116">**SMTP address component**</span></span>|<span data-ttu-id="5a71f-117">**Propiedad MAPI**</span><span class="sxs-lookup"><span data-stu-id="5a71f-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5a71f-118">_nombre para mostrar_ para todos los destinatarios</span><span class="sxs-lookup"><span data-stu-id="5a71f-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="5a71f-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5a71f-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="5a71f-120">_nombre para mostrar_ para el campo</span><span class="sxs-lookup"><span data-stu-id="5a71f-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="5a71f-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5a71f-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="5a71f-122">_nombre para mostrar_ para el campo de remitente</span><span class="sxs-lookup"><span data-stu-id="5a71f-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="5a71f-123">**PR_SENT_REPRESENTING_NAME de MAPI** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5a71f-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="5a71f-124">_dirección de correo electrónico_</span><span class="sxs-lookup"><span data-stu-id="5a71f-124">_email-address_</span></span> <br/> |<span data-ttu-id="5a71f-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5a71f-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="5a71f-126">implícitas, siempre "SMTP"</span><span class="sxs-lookup"><span data-stu-id="5a71f-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="5a71f-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5a71f-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="5a71f-128">Si no hay ningún nombre para mostrar para una dirección de correo entrante, la dirección de correo electrónico completa debe usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="5a71f-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="5a71f-129">El tipo de dirección siempre es SMTP.</span><span class="sxs-lookup"><span data-stu-id="5a71f-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="5a71f-130">Las propiedades de destinatarios se toman de la tabla de destinatarios del mensaje MAPI; propiedades de remitente se toman desde el propio mensaje.</span><span class="sxs-lookup"><span data-stu-id="5a71f-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

