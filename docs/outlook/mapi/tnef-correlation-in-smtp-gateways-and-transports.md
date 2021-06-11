---
title: Correlación de TNEF en puertas de enlace SMTP y transportes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413671"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="39bb2-103">Correlación de TNEF en puertas de enlace SMTP y transportes</span><span class="sxs-lookup"><span data-stu-id="39bb2-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="39bb2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39bb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39bb2-105">Las puertas de enlace y los transportes que se conectan a sistemas basados en Internet, los que usan SMTP, usan el valor del encabezado SMTP MessageID y la propiedad **PR_TNEF_CORRELATION_KEY** para implementar la correlación TNEF.</span><span class="sxs-lookup"><span data-stu-id="39bb2-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="39bb2-106">El valor del encabezado MessageID del mensaje saliente debe copiarse en la propiedad **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) y codificarse en el atributo [attMAPIProps](attmapiprops.md) de la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="39bb2-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="39bb2-107">Tenga en **cuenta PR_TNEF_CORRELATION_KEY** es una propiedad binaria, mientras que MessageID es una cadena; el terminador nulo debe incluirse en la copia y en la comparación.</span><span class="sxs-lookup"><span data-stu-id="39bb2-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="39bb2-108">Esta técnica la usa todo el software de Microsoft que conecta sistemas de mensajería basados en MAPI a Internet, como Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="39bb2-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="39bb2-109">Esta técnica debe ser usada por las puertas de enlace SMTP y los transportes que se conectan a sistemas que admiten clientes MAPI para maximizar la interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="39bb2-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

