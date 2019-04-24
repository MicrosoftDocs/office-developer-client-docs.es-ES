---
title: Responsabilidades de la asignación de puerta de enlace
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 214d24bb0b0af525d5e2588c556c37cf720364a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342801"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="7660e-103">Responsabilidades de la asignación de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="7660e-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="7660e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7660e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7660e-105">Cuando una puerta de enlace compatible con MAPI recibe un mensaje que contiene propiedades con nombre en uno de los conjuntos de propiedades especiales designados para contener propiedades asignables a la puerta de enlace, la puerta de enlace debe asignar todas las propiedades al protocolo del sistema de mensajería de destino.</span><span class="sxs-lookup"><span data-stu-id="7660e-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="7660e-106">Aunque MAPI recomienda que las puertas de enlace controlen todas las propiedades con nombre en los conjuntos de propiedades especiales, se espera que las puertas de enlace controlen sólo dos: la dirección de correo electrónico y el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="7660e-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="7660e-107">Debido a que las propiedades de dirección de correo electrónico y tipo de dirección afectan directamente a la transmisión de mensajes, es fundamental que las puertas de enlace admitan la asignación de estas dos propiedades.</span><span class="sxs-lookup"><span data-stu-id="7660e-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="7660e-108">Como las claves de búsqueda constan de la dirección y el tipo de dirección de un usuario, también deben traducirse si es posible.</span><span class="sxs-lookup"><span data-stu-id="7660e-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="7660e-109">No se espera que los identificadores de entrada se traten con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="7660e-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="7660e-110">Para habilitar la asignación de un identificador de entrada que se origina en un sistema de mensajería a un identificador de entrada que puede ser utilizado por otro sistema de mensajería, la puerta de enlace debe ser capaz de usar el formato de ambos sistemas.</span><span class="sxs-lookup"><span data-stu-id="7660e-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="7660e-111">Como la mayoría de las puertas de enlace no conocen los formatos de identificador de entrada, la conversión de los identificadores de entrada es poco frecuente.</span><span class="sxs-lookup"><span data-stu-id="7660e-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="7660e-112">Otra propiedad asignable que no se espera que se traduzca con frecuencia es el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="7660e-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="7660e-113">Las puertas de enlace deben almacenar los nombres para mostrar y transmitirlos, pero no necesariamente traducirlos.</span><span class="sxs-lookup"><span data-stu-id="7660e-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

