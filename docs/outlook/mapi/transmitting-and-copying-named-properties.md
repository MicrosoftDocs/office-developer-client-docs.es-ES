---
title: Transmitir y copiar propiedades con nombre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1c225712e354d72b79313ee4c3f36da55f11b0a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587519"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="922cd-103">Transmitir y copiar propiedades con nombre</span><span class="sxs-lookup"><span data-stu-id="922cd-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="922cd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="922cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="922cd-105">Siempre que se envía una propiedad con nombre, mover o copian, el nombre permanece constante, pero debe cambiar el identificador para adherirse a la asignación del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="922cd-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="922cd-106">La única excepción a esta regla es cuando el origen y destino tienen la misma firma de asignación, realizar reasignación innecesarios.</span><span class="sxs-lookup"><span data-stu-id="922cd-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="922cd-107">Es responsabilidad del proveedor de transporte para volver a asignar los nombres de propiedades con nombre transmitidos a identificadores adecuados que funcionan en el destino.</span><span class="sxs-lookup"><span data-stu-id="922cd-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="922cd-108">El proveedor de transporte envío no sabe cuál es la asignación correcta en el destino; se debe transmitir los nombres y se basan en el proveedor de transporte receptora para asignarlos a identificadores que funcionan.</span><span class="sxs-lookup"><span data-stu-id="922cd-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="922cd-109">La implementación de MAPI de TNEF controla la reasignación de propiedades con nombre para los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="922cd-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="922cd-110">Los proveedores de transporte pueden controlar la reasignación manualmente o usar la implementación de TNEF.</span><span class="sxs-lookup"><span data-stu-id="922cd-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="922cd-111">Una reasignación similar de propiedades con nombre debe producirse cuando estas propiedades se copian entre almacenes de mensajes.</span><span class="sxs-lookup"><span data-stu-id="922cd-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="922cd-112">Sin embargo, debido a que los proveedores de almacén de mensaje pueden recuperar el nombre de la asignación del identificador de destino, pueden volver a asignar las propiedades inmediatamente y no tiene que se basan en el almacén de mensajes de destino.</span><span class="sxs-lookup"><span data-stu-id="922cd-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="922cd-113">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="922cd-113">See also</span></span>



[<span data-ttu-id="922cd-114">Con el nombre de las propiedades de MAPI</span><span class="sxs-lookup"><span data-stu-id="922cd-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

