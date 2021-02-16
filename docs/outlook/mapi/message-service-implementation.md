---
title: Implementación del servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434035"
---
# <a name="message-service-implementation"></a><span data-ttu-id="6c419-103">Implementación del servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="6c419-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="6c419-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c419-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c419-105">Un servicio de mensajes es uno o más proveedores de servicios relacionados agrupados con el fin de simplificar la instalación y la configuración.</span><span class="sxs-lookup"><span data-stu-id="6c419-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="6c419-106">Todos los proveedores de servicios deben incluirse en un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="6c419-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="6c419-107">Para implementar un servicio de mensajes con uno o varios proveedores, use el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="6c419-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="6c419-108">Diseñe el servicio de mensajes, determinando el número y el tipo de proveedores de servicios que se incluirán.</span><span class="sxs-lookup"><span data-stu-id="6c419-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="6c419-109">Para obtener más información acerca de cómo diseñar un servicio de mensajes, vea [El diseño de un servicio de mensajes.](designing-a-message-service.md)</span><span class="sxs-lookup"><span data-stu-id="6c419-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="6c419-110">Cree un programa de instalación para instalar los proveedores de servicios en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="6c419-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="6c419-111">Para obtener más información acerca de cómo escribir un programa de instalación del servicio de mensajes, vea [Compatibilidad con la instalación del servicio de mensajes.](supporting-message-service-installation.md)</span><span class="sxs-lookup"><span data-stu-id="6c419-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="6c419-112">Cree una función de punto de entrada para realizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="6c419-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="6c419-113">Para obtener más información acerca de cómo escribir una función de punto de entrada del servicio de mensajes, vea Compatibilidad con la configuración del servicio [de](supporting-message-service-configuration.md) mensajes y [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="6c419-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="6c419-114">Cree un archivo de encabezado público que contenga las etiquetas de propiedad y las descripciones de valores válidos para las propiedades personalizadas compatibles con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="6c419-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6c419-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6c419-115">See also</span></span>



[<span data-ttu-id="6c419-116">Proveedores de servicios MAPI</span><span class="sxs-lookup"><span data-stu-id="6c419-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

