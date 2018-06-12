---
title: Implementación del servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 6ba2f9542fd021c544d73d8208ed356a7bf95309
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818389"
---
# <a name="message-service-implementation"></a><span data-ttu-id="87b20-103">Implementación del servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="87b20-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="87b20-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87b20-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="87b20-105">Un servicio de mensajes es uno o más proveedores de servicios relacionadas agrupados con el propósito de simplificar la instalación y configuración.</span><span class="sxs-lookup"><span data-stu-id="87b20-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="87b20-106">Todos los proveedores de servicios deben incluirse en un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="87b20-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="87b20-107">Para implementar un servicio de mensajes con uno o varios proveedores, use el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="87b20-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="87b20-108">Diseñar el servicio de mensajes, determinar el número y el tipo de proveedores de servicios que se incluya.</span><span class="sxs-lookup"><span data-stu-id="87b20-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="87b20-109">Para obtener más información acerca de cómo diseñar un servicio de mensajes, vea [diseñar un servicio de mensajes](designing-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="87b20-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="87b20-110">Crear un programa de instalación para instalar a los proveedores de servicios en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="87b20-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="87b20-111">Para obtener más información acerca de cómo escribir un programa de instalación del servicio de mensajes, vea [Compatibilidad con mensaje de servicio de instalación](supporting-message-service-installation.md).</span><span class="sxs-lookup"><span data-stu-id="87b20-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="87b20-112">Crear una función de punto de entrada para realizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="87b20-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="87b20-113">Para obtener más información acerca de cómo escribir una entrada de mensajes de servicio de función de punto, vea [Compatibilidad con configuración del servicio de mensajes](supporting-message-service-configuration.md) y [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="87b20-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="87b20-114">Cree un archivo de encabezado público que contiene las etiquetas de propiedad y descripciones de los valores válidos para las propiedades personalizadas que es compatible con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="87b20-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="87b20-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="87b20-115">See also</span></span>



[<span data-ttu-id="87b20-116">Proveedores de servicios de MAPI</span><span class="sxs-lookup"><span data-stu-id="87b20-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

