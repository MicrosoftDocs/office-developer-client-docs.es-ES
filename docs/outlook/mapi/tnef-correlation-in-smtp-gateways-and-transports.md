---
title: Correlación TNEF de puertas de enlace SMTP y transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ec1d826ee2b3b46685a2c03dfaf45d2843869cc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820867"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="f944c-103">Correlación TNEF de puertas de enlace SMTP y transporte</span><span class="sxs-lookup"><span data-stu-id="f944c-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="f944c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f944c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f944c-105">Las puertas de enlace y los transportes que se conectan a internet sistemas basados en, aquellos que usan SMTP, use el valor de encabezado de SMTP MessageID y la propiedad **PR_TNEF_CORRELATION_KEY** para implementar la correlación de TNEF.</span><span class="sxs-lookup"><span data-stu-id="f944c-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="f944c-106">El valor del encabezado del mensaje saliente MessageID debe se copia a la propiedad **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) y codificado en el atributo [attMAPIProps](attmapiprops.md) de la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="f944c-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="f944c-107">Tenga en cuenta que **PR_TNEF_CORRELATION_KEY** es una propiedad binaria, mientras que el identificador del mensaje es una cadena; el terminador nulo se debe incluir en la copia y en la comparación.</span><span class="sxs-lookup"><span data-stu-id="f944c-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="f944c-108">Esta técnica se usa en todo el software de Microsoft que se conecta a sistemas de mensajería basado en MAPI a Internet, como Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f944c-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="f944c-109">Las puertas de enlace SMTP y los transportes que se conectan a los sistemas que admiten los clientes MAPI para maximizar la interoperabilidad debe usar esta técnica.</span><span class="sxs-lookup"><span data-stu-id="f944c-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

