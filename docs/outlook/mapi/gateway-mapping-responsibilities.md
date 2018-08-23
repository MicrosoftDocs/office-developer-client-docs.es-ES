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
ms.openlocfilehash: 91c1d9293108b96fde43b769c97ec673f82a8cb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563033"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="66d15-103">Responsabilidades de la asignación de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="66d15-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="66d15-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66d15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66d15-105">Cuando una puerta de enlace compatible con MAPI recibe un mensaje que contiene propiedades con nombre en uno de los conjuntos de propiedades especiales designados para contener propiedades pueda asignar la puerta de enlace, la puerta de enlace debe asignar todas las propiedades del protocolo del sistema de mensajería de destino.</span><span class="sxs-lookup"><span data-stu-id="66d15-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="66d15-106">Aunque MAPI, se recomienda que las puertas de enlace controlan con nombre de todas las propiedades en los conjuntos de propiedades especiales, las puertas de enlace se espera que controlen sólo dos: dirección y tipo de dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="66d15-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="66d15-107">Debido a que la dirección de correo electrónico y las propiedades de tipo de dirección afectan directamente a la transmisión de mensajes, es fundamental que las puertas de enlace compatible con la asignación de estas dos propiedades.</span><span class="sxs-lookup"><span data-stu-id="66d15-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="66d15-108">Debido a que las claves de búsqueda se componen de tipo de dirección y la dirección de un usuario, también se deben traducir si es posible.</span><span class="sxs-lookup"><span data-stu-id="66d15-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="66d15-109">No se esperan que los identificadores de entrada se controlarán con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="66d15-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="66d15-110">Para habilitar la asignación de un identificador de entrada que se origina en un sistema de mensajería a un identificador de entrada que se puede usar por otro sistema de mensajería, la puerta de enlace debe ser capaz de utilizar el formato de ambos sistemas.</span><span class="sxs-lookup"><span data-stu-id="66d15-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="66d15-111">Debido a que la mayoría de las puertas de enlace no son conscientes de formatos de identificador de entrada, la traducción de los identificadores de entrada es poco habitual.</span><span class="sxs-lookup"><span data-stu-id="66d15-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="66d15-112">Otra propiedad pueda asignar que no se espera que se debe traducir con frecuencia es el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="66d15-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="66d15-113">Las puertas de enlace deben almacenar los nombres para mostrar y transmitirlos, pero no necesariamente traducir a ellos.</span><span class="sxs-lookup"><span data-stu-id="66d15-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

