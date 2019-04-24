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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356920"
---
# <a name="message-service-implementation"></a><span data-ttu-id="835c8-103">Implementación del servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="835c8-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="835c8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="835c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="835c8-105">Un servicio de mensajes es uno o varios proveedores de servicios relacionados agrupados con el propósito de simplificar la instalación y la configuración.</span><span class="sxs-lookup"><span data-stu-id="835c8-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="835c8-106">Todos los proveedores de servicios deben incluirse en un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="835c8-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="835c8-107">Para implementar un servicio de mensajes con uno o más proveedores, use el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="835c8-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="835c8-108">Diseñar el servicio de mensajes, determinar el número y el tipo de proveedores de servicios que se incluirán.</span><span class="sxs-lookup"><span data-stu-id="835c8-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="835c8-109">Para obtener más información acerca de cómo diseñar un servicio de mensajes, vea [Designing a Message Service](designing-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="835c8-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="835c8-110">Cree un programa de instalación para instalar los proveedores de servicios en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="835c8-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="835c8-111">Para obtener más información acerca de cómo escribir un programa de instalación del servicio de mensajes, consulte [support Message Service Installation](supporting-message-service-installation.md).</span><span class="sxs-lookup"><span data-stu-id="835c8-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="835c8-112">Cree una función de punto de entrada para realizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="835c8-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="835c8-113">Para obtener más información acerca de la escritura de una función de punto de entrada del servicio de mensajes, consulte [supportIng Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="835c8-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="835c8-114">Cree un archivo de encabezado público que contenga las etiquetas de propiedades y descripciones de los valores válidos para las propiedades personalizadas admitidas por el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="835c8-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="835c8-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="835c8-115">See also</span></span>



[<span data-ttu-id="835c8-116">Proveedores de servicios MAPI</span><span class="sxs-lookup"><span data-stu-id="835c8-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

