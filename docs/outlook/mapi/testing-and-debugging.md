---
title: Pruebas y dePuración
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0afceb1f-9086-4cc9-8ce4-fb9256a81a9c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8e1f15ae354894aede4e8418e6428d0524ccb70d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316488"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="b40c7-103">Pruebas y dePuración</span><span class="sxs-lookup"><span data-stu-id="b40c7-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="b40c7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b40c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b40c7-105">Las estrategias de pruebas varían en función de si está desarrollando un cliente o proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="b40c7-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="b40c7-106">Debido a que una aplicación cliente requiere que uno o más proveedores de servicios funcionen, los clientes deben probarse en un entorno con diferentes conjuntos de proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="b40c7-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="b40c7-107">Sin embargo, los proveedores de servicios deben probarse de forma aislada antes de integrarse con otros proveedores.</span><span class="sxs-lookup"><span data-stu-id="b40c7-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="b40c7-108">MAPI proporciona herramientas que tienen como objetivo probar las características de un proveedor de servicios de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="b40c7-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="b40c7-109">La aplicación de ejemplo [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154) muestra cómo probar las características de un proveedor de la libreta de direcciones y funciona con un proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b40c7-109">The [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b40c7-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="b40c7-110">See also</span></span>



[<span data-ttu-id="b40c7-111">Información general sobre programación de MAPI</span><span class="sxs-lookup"><span data-stu-id="b40c7-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="b40c7-112">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="b40c7-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

