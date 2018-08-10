---
title: Correlación TNEF de puertas de enlace X.400 y transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ea5ca41ef21c72377ade72370e0aee1b313c92d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820864"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="5594e-103">Correlación TNEF de puertas de enlace X.400 y transporte</span><span class="sxs-lookup"><span data-stu-id="5594e-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="5594e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5594e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5594e-105">Las puertas de enlace y los transportes que se conectan a sistemas basados en X.400, use el valor del atributo IM_THIS_IPM X.400 y el atributo TNEF **attMessageID** para implementar la correlación de TNEF.</span><span class="sxs-lookup"><span data-stu-id="5594e-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="5594e-106">El valor del atributo IM_THIS_IPM del mensaje saliente se copia a **attMessageID** en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="5594e-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="5594e-107">El atributo IM_THIS_IPM X.400 normalmente es una cadena, mientras que el atributo TNEF **attMessageID** es una cadena de dígitos hexadecimales que representa un valor binario.</span><span class="sxs-lookup"><span data-stu-id="5594e-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="5594e-108">Por lo tanto, cada carácter en el atributo IM_THIS_IPM X.400, incluido el carácter null final, se debe convertir en una cadena hexadecimal 2 caracteres que representa el valor ASCII del carácter.</span><span class="sxs-lookup"><span data-stu-id="5594e-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="5594e-109">Por ejemplo, si el atributo IM_THIS_IPM X.400 es la cadena siguiente:</span><span class="sxs-lookup"><span data-stu-id="5594e-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="5594e-110">3030322D3030312D305337533A3A3936303631312D313533373030</span><span class="sxs-lookup"><span data-stu-id="5594e-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="5594e-111">a continuación, el valor de **attMessageID** sería la siguiente secuencia de dígitos hexadecimales:</span><span class="sxs-lookup"><span data-stu-id="5594e-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="5594e-112">33 30 33 30 33 32 32 44</span><span class="sxs-lookup"><span data-stu-id="5594e-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="5594e-113">33 30 33 30 33 31 32 44</span><span class="sxs-lookup"><span data-stu-id="5594e-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="5594e-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="5594e-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="5594e-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="5594e-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="5594e-116">33 30 33 36 33 31 33 31</span><span class="sxs-lookup"><span data-stu-id="5594e-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="5594e-117">32 44 33 31 33 35 33 33</span><span class="sxs-lookup"><span data-stu-id="5594e-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="5594e-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="5594e-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="5594e-119">Esta técnica se usa en el conector de X.400 de Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5594e-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="5594e-120">Las puertas de enlace X.400 y los transportes que se conectan a Microsoft Exchange Server para maximizar la interoperabilidad debe usar esta técnica.</span><span class="sxs-lookup"><span data-stu-id="5594e-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="5594e-121">Para mayor compatibilidad con el software de Microsoft futuro, así como está presente, el atributo IM_THIS_IPM X.400 también se debe copiar en la propiedad **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5594e-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="5594e-122">Sin embargo, puesto que **PR_TNEF_CORRELATION_KEY** es una propiedad binaria, es necesaria ninguna traducción en una cadena hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="5594e-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  
