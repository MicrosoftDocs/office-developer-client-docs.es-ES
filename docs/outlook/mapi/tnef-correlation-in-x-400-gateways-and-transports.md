---
title: Correlación TNEF en puertas de enlace x.400 y transportes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e08f16ff60a282f1be3adf93d858471e38d19957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406377"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="a26a0-103">Correlación TNEF en puertas de enlace x.400 y transportes</span><span class="sxs-lookup"><span data-stu-id="a26a0-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="a26a0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a26a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a26a0-105">Las puertas de enlace y los transportes que se conectan a sistemas basados en X.400, usan el valor del atributo X.400 de IM_THIS_IPM y el atributo **TNEF attMessageID** para implementar la correlación TNEF.</span><span class="sxs-lookup"><span data-stu-id="a26a0-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="a26a0-106">El valor del atributo IM_THIS_IPM del mensaje saliente se copia en **attMessageID** en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="a26a0-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="a26a0-107">El IM_THIS_IPM X.400 suele ser una cadena, mientras que el atributo **TNEF attMessageID** es una cadena de dígitos hexadecimales que representa un valor binario.</span><span class="sxs-lookup"><span data-stu-id="a26a0-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="a26a0-108">Por lo tanto, cada carácter del atributo IM_THIS_IPM X.400, incluido el carácter nulo de terminación, debe convertirse en una cadena hexadecimal de 2 caracteres que represente el valor ASCII de ese carácter.</span><span class="sxs-lookup"><span data-stu-id="a26a0-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="a26a0-109">Por ejemplo, si el IM_THIS_IPM X.400 es la siguiente cadena:</span><span class="sxs-lookup"><span data-stu-id="a26a0-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="a26a0-110">3030322D3030312D305337533A3A3936303631312D3135337303030</span><span class="sxs-lookup"><span data-stu-id="a26a0-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="a26a0-111">a continuación, el **valor de attMessageID** sería la siguiente secuencia de dígitos hexadecimales:</span><span class="sxs-lookup"><span data-stu-id="a26a0-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="a26a0-112">33 30 33 30 33 32 32 44</span><span class="sxs-lookup"><span data-stu-id="a26a0-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="a26a0-113">33 30 33 30 33 31 32 44</span><span class="sxs-lookup"><span data-stu-id="a26a0-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="a26a0-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="a26a0-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="a26a0-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="a26a0-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="a26a0-116">33 30 33 36 33 31 33 31</span><span class="sxs-lookup"><span data-stu-id="a26a0-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="a26a0-117">32 44 33 31 33 35 33 33</span><span class="sxs-lookup"><span data-stu-id="a26a0-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="a26a0-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="a26a0-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="a26a0-119">Esta técnica la usa el Microsoft Exchange Server X.400 Connector.</span><span class="sxs-lookup"><span data-stu-id="a26a0-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="a26a0-120">Esta técnica debe ser usada por las puertas de enlace X.400 y los transportes que se conectan a Microsoft Exchange Server para maximizar la interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="a26a0-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="a26a0-121">Para mayor compatibilidad con el software de Microsoft futuro y presente, el atributo IM_THIS_IPM X.400 también debe copiarse en la propiedad **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a26a0-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="a26a0-122">Sin embargo, **PR_TNEF_CORRELATION_KEY** es una propiedad binaria, no es necesario traducir a una cadena hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="a26a0-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  

