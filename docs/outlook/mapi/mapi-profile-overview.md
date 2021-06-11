---
title: Introducción a perfiles MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328171"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="0d8b1-103">Introducción a perfiles MAPI</span><span class="sxs-lookup"><span data-stu-id="0d8b1-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="0d8b1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d8b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d8b1-105">Un perfil es una colección de información sobre los servicios de mensajes y los proveedores de servicios que un usuario de una aplicación cliente desea que esté disponible durante una sesión MAPI determinada.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="0d8b1-106">Cada usuario tiene al menos un perfil; muchos usuarios mantienen varios.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="0d8b1-107">Por ejemplo, un usuario puede tener un perfil para trabajar con un servicio de almacén de mensajes basado en servidor y otro perfil para trabajar con un servicio de almacén de mensajes en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="0d8b1-108">Es posible que un usuario quiera tener acceso a un conjunto de sistemas de mensajería mediante los servicios de transporte adecuados durante parte del día y otro conjunto para el resto del día.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="0d8b1-109">Los perfiles proporcionan una forma flexible de seleccionar combinaciones de servicios del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="0d8b1-110">Los perfiles pueden tener nombres de hasta 64 caracteres alfanuméricos de longitud.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="0d8b1-111">Los nombres pueden incluir caracteres de énfal, el carácter de subrayado y espacios incrustados, y no pueden incluir espacios iniciales o finales.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="0d8b1-112">Los perfiles se organizan jerárquicamente y se dividen en secciones, con una sección para cada servicio de mensajes y una sección para cada proveedor de servicios de un servicio.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="0d8b1-113">Las secciones relacionadas están vinculadas, lo que facilita la navegación por la información.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="0d8b1-114">Cada sección contiene una serie de entradas que MAPI o una aplicación cliente usa para la configuración.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="0d8b1-115">Las entradas incluidas en un perfil varían del servicio de mensajes al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="0d8b1-116">Algunas de las entradas comunes incluyen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0d8b1-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="0d8b1-117">Nombre de cada servicio de mensajes o proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="0d8b1-118">Nombre de las DLL que contienen proveedores de servicios y servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="0d8b1-119">Nombre de la función de punto de entrada de cada servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="0d8b1-120">Una lista de los proveedores de servicios que forma cada servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="0d8b1-121">Los perfiles se pueden crear en el momento de la instalación, cuando MAPI o un servicio de mensajes se cargan en un equipo o en cualquier momento posterior.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="0d8b1-122">MAPI proporciona el Asistente para perfiles para la administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="0d8b1-123">El Asistente para perfiles es una aplicación que crea nuevos perfiles con una cantidad mínima de trabajo.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="0d8b1-124">El asistente usa valores predeterminados para la configuración siempre que sea posible, lo que ahorra tiempo y esfuerzo a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="0d8b1-125">Los usuarios escriben valores solo cuando es absolutamente necesario.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="0d8b1-126">Para obtener más información, vea [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="0d8b1-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="0d8b1-127">También puede usar la herramienta de personalización Office para crear un perfil nuevo.</span><span class="sxs-lookup"><span data-stu-id="0d8b1-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="0d8b1-128">Para obtener más información, vea la [Herramienta de personalización de Office](https://go.microsoft.com/fwlink/?LinkId=123000).</span><span class="sxs-lookup"><span data-stu-id="0d8b1-128">For more information, see [Office Customization Tool](https://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d8b1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d8b1-129">See also</span></span>



[<span data-ttu-id="0d8b1-130">Características y arquitectura MAPI</span><span class="sxs-lookup"><span data-stu-id="0d8b1-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

