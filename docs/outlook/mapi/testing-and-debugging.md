---
title: Pruebas y depuración
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0afceb1f-9086-4cc9-8ce4-fb9256a81a9c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ae9b49717fd7981d653e9852ed02d50bef7c7846
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590690"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="46c37-103">Pruebas y depuración</span><span class="sxs-lookup"><span data-stu-id="46c37-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="46c37-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46c37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46c37-105">Las estrategias de pruebas varían dependiendo de si está desarrollando un proveedor de cliente o servicio.</span><span class="sxs-lookup"><span data-stu-id="46c37-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="46c37-106">Debido a que una aplicación cliente requiere uno o más proveedores de servicio para que funcione, los clientes deben probarse en un entorno con distintos conjuntos de proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="46c37-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="46c37-107">Proveedores de servicios, sin embargo, se deben probar de forma aislada antes de que se está integrado con otros proveedores.</span><span class="sxs-lookup"><span data-stu-id="46c37-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="46c37-108">MAPI proporciona herramientas que están diseñadas para probar las características de un proveedor de servicio de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="46c37-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="46c37-109">La aplicación de ejemplo [MFCMAPI](http://go.microsoft.com/fwlink/?LinkId=124154) muestra cómo probar las características de un proveedor de la libreta de direcciones y funciona con un mensaje de proveedor de almacén.</span><span class="sxs-lookup"><span data-stu-id="46c37-109">The [MFCMAPI](http://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46c37-110">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="46c37-110">See also</span></span>



[<span data-ttu-id="46c37-111">Informaci�n general sobre programaci�n de MAPI</span><span class="sxs-lookup"><span data-stu-id="46c37-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="46c37-112">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="46c37-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

