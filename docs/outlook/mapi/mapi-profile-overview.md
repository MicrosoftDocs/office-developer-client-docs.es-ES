---
title: Información general sobre el perfil MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a34c21e20fa45cd3265ec42c9d992eb828203f66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563917"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="aa488-103">Información general sobre el perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="aa488-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="aa488-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa488-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa488-105">Un perfil es una colección de información acerca de los servicios de mensaje y los proveedores de servicios que un usuario de una aplicación de cliente desea estar disponibles durante una sesión MAPI en particular.</span><span class="sxs-lookup"><span data-stu-id="aa488-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="aa488-106">Cada usuario tiene al menos un perfil; muchos usuarios mantienen varias.</span><span class="sxs-lookup"><span data-stu-id="aa488-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="aa488-107">Por ejemplo, un usuario puede tener un perfil para que funcione con un servicio de almacenamiento de mensajes basado en servidor y otro perfil para que funcione con un servicio de almacenamiento de mensajes en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="aa488-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="aa488-108">Un usuario es posible que desee tener acceso a un conjunto de sistemas de mensajería mediante el uso de los servicios de transporte adecuados para la parte del día y otro conjunto para el resto del día.</span><span class="sxs-lookup"><span data-stu-id="aa488-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="aa488-109">Los perfiles proporcionan una forma flexible para seleccionar combinaciones de servicios del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="aa488-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="aa488-110">Los perfiles pueden tener nombres hasta 64 caracteres alfanuméricos de longitud.</span><span class="sxs-lookup"><span data-stu-id="aa488-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="aa488-111">Los nombres pueden incluir caracteres de énfasis, el carácter de subrayado y espacios incrustados y no pueden incluir espacios iniciales ni finales.</span><span class="sxs-lookup"><span data-stu-id="aa488-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="aa488-112">Los perfiles se organiza jerárquicamente y divididos en secciones, con una sección para cada servicio de mensajes y una sección para cada proveedor de servicios en un servicio.</span><span class="sxs-lookup"><span data-stu-id="aa488-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="aa488-113">Las secciones relacionadas están vinculadas, haciendo que sea más fácil de navegar por la información.</span><span class="sxs-lookup"><span data-stu-id="aa488-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="aa488-114">Cada sección contiene una serie de entradas que MAPI o una aplicación cliente que se usa para la configuración.</span><span class="sxs-lookup"><span data-stu-id="aa488-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="aa488-115">Los movimientos incluidos en un perfil varían de servicio de mensajes al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="aa488-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="aa488-116">Algunas de las entradas comunes incluyen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="aa488-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="aa488-117">El nombre de cada servicio de mensajes o el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="aa488-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="aa488-118">El nombre de los archivos DLL que contienen los proveedores de servicios y los servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="aa488-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="aa488-119">El nombre de la función de punto de entrada del servicio de cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa488-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="aa488-120">Una lista de los proveedores de servicios que componen cada servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="aa488-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="aa488-121">Los perfiles se pueden crear en tiempo de instalación, cuando se carga MAPI o un servicio de mensajes en un equipo, o en cualquier momento posterior.</span><span class="sxs-lookup"><span data-stu-id="aa488-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="aa488-122">MAPI proporciona al Asistente para perfiles de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="aa488-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="aa488-123">El Asistente para perfiles es una aplicación que crea nuevos perfiles con una cantidad mínima de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa488-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="aa488-124">El asistente usa los valores predeterminados para la configuración siempre que sea posible, ahorrando esfuerzo y tiempo a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="aa488-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="aa488-125">Los usuarios escriben valores sólo cuando sea absolutamente necesario.</span><span class="sxs-lookup"><span data-stu-id="aa488-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="aa488-126">Para obtener más información, vea [creación de un perfil mediante el Asistente para perfiles](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="aa488-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="aa488-127">También puede usar la herramienta de personalización de Office para crear un nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="aa488-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="aa488-128">Para obtener más información, vea [Office Customization Tool](http://go.microsoft.com/fwlink/?LinkId=123000).</span><span class="sxs-lookup"><span data-stu-id="aa488-128">For more information, see [Office Customization Tool](http://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa488-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="aa488-129">See also</span></span>



[<span data-ttu-id="aa488-130">Arquitectura y las características MAPI</span><span class="sxs-lookup"><span data-stu-id="aa488-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

