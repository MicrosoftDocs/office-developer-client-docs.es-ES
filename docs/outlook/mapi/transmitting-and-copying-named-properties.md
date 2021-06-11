---
title: Transmisión y copia de propiedades con nombre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6534e7344a62717e406c112249d26407b0852d93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437780"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="a94ca-103">Transmisión y copia de propiedades con nombre</span><span class="sxs-lookup"><span data-stu-id="a94ca-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="a94ca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a94ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a94ca-105">Siempre que se envía, mueve o copia una propiedad con nombre, el nombre permanece constante, pero el identificador debe cambiar para cumplir con la asignación del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="a94ca-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="a94ca-106">La única excepción a esta regla es cuando el origen y el destino tienen la misma firma de asignación, lo que hace innecesaria la nueva asignación.</span><span class="sxs-lookup"><span data-stu-id="a94ca-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="a94ca-107">Es responsabilidad del proveedor de transporte volver a asignar los nombres de las propiedades con nombre transmitidas a los identificadores adecuados que funcionan en el destino.</span><span class="sxs-lookup"><span data-stu-id="a94ca-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="a94ca-108">El proveedor de transporte de envío no puede saber cuál es la asignación correcta en el destino; debe transmitir los nombres y confiar en el proveedor de transporte de recepción para asignarlos a los identificadores que funcionan.</span><span class="sxs-lookup"><span data-stu-id="a94ca-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="a94ca-109">La implementación MAPI de TNEF controla la remapping de propiedades con nombre para proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="a94ca-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="a94ca-110">Los proveedores de transporte pueden controlar la remapping manualmente o usar la implementación de TNEF.</span><span class="sxs-lookup"><span data-stu-id="a94ca-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="a94ca-111">Cuando estas propiedades se copian entre almacenes de mensajes, debe producirse una nueva remapping similar de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="a94ca-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="a94ca-112">Sin embargo, como los proveedores de almacén de mensajes pueden recuperar el nombre a la asignación de identificadores del destino, pueden volver a asignar las propiedades de inmediato y no tienen que depender del almacén de mensajes de destino.</span><span class="sxs-lookup"><span data-stu-id="a94ca-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a94ca-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="a94ca-113">See also</span></span>



[<span data-ttu-id="a94ca-114">Propiedades con nombre MAPI</span><span class="sxs-lookup"><span data-stu-id="a94ca-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

