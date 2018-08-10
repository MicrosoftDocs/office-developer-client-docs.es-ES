---
title: Compatibilidad con la configuración del servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e1782f3c20c1741e0e4b1859f1b29d835444009c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820784"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="1358d-103">Compatibilidad con la configuración del servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="1358d-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="1358d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1358d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1358d-105">Para admitir la configuración del servicio de mensajes, use el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="1358d-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="1358d-106">Implementar una función de punto de entrada que se ajusta al prototipo [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="1358d-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="1358d-107">Funciones de punto de entrada de servicio de mensaje administración el acceso a datos de configuración y se denominan en las siguientes circunstancias:</span><span class="sxs-lookup"><span data-stu-id="1358d-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="1358d-108">Cuando un cliente inicia sesión para recuperar información para configurar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1358d-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="1358d-109">Cuando un cliente desea ver o cambiar una propiedad de configuración.</span><span class="sxs-lookup"><span data-stu-id="1358d-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="1358d-110">Aunque la mayoría de los servicios de mensaje proporcionará las funciones de punto de entrada, como deberían, estas funciones no son estrictamente necesarias.</span><span class="sxs-lookup"><span data-stu-id="1358d-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="1358d-111">Servicios de mensajes pueden proporcionar acceso a datos de configuración de otras maneras.</span><span class="sxs-lookup"><span data-stu-id="1358d-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="1358d-112">Sin embargo, el uso de una función de punto de entrada estandariza y simplifica el proceso de configuración.</span><span class="sxs-lookup"><span data-stu-id="1358d-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="1358d-113">MAPI espera que funciones del punto de entrada de servicio de todos los mensajes que puedan almacenar y recuperar las propiedades de las secciones de perfil que están asociadas con su servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1358d-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="1358d-114">Puede admitir esta funcionalidad de forma interactiva, mediante programación, o ambos de forma interactiva y mediante programación.</span><span class="sxs-lookup"><span data-stu-id="1358d-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="1358d-115">Para admitir la configuración interactiva, proporcionar una hoja de propiedades que se muestran las propiedades necesarios para configurar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1358d-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="1358d-116">Como una opción, también puede proporcionar las hojas de propiedades para cada proveedor configurable.</span><span class="sxs-lookup"><span data-stu-id="1358d-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="1358d-117">Algunos servicios de mensaje restricción a los usuarios a una vista de solo lectura de propiedades de configuración; otros servicios de mensaje permiten a los usuarios realizar cambios.</span><span class="sxs-lookup"><span data-stu-id="1358d-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="1358d-118">Para admitir la configuración mediante programación, la función de punto de entrada de servicio de mensaje debe poder funcionar sin intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="1358d-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="1358d-119">Si el servicio de mensajes se puede llamar mediante el Asistente para perfiles, debe admitir la configuración mediante programación.</span><span class="sxs-lookup"><span data-stu-id="1358d-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="1358d-120">Si el servicio de mensajes no permitir que se pueden configurar mediante el Asistente para perfiles, puede elegir si desea o no admite la configuración mediante programación.</span><span class="sxs-lookup"><span data-stu-id="1358d-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="1358d-121">Para obtener más información acerca de cómo admitir la configuración en una entrada de mensajes de servicio punto (función), consulte [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="1358d-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="1358d-122">Publicar el nombre de la función de punto de entrada de servicio de mensaje en el archivo de configuración Mapisvc.inf mediante la inclusión de la siguiente entrada en la sección servicio de mensaje:</span><span class="sxs-lookup"><span data-stu-id="1358d-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="1358d-123">Crear uno o varios (propiedad) hoja cuadros de diálogo para mostrar los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="1358d-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="1358d-124">Si desea permitir que el Asistente para perfiles configurar el servicio de mensajes, realice las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="1358d-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="1358d-125">Implementar una función de punto de entrada que se ajusta al prototipo [WIZARDENTRY](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="1358d-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="1358d-126">Implementar un procedimiento de cuadros de diálogo de Windows estándar que se ajusta al prototipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="1358d-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="1358d-127">Mejorar la función de punto de entrada de servicio de mensaje para responder a eventos adicionales.</span><span class="sxs-lookup"><span data-stu-id="1358d-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1358d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1358d-128">See also</span></span>

- [<span data-ttu-id="1358d-129">Implementación de servicios de mensajería</span><span class="sxs-lookup"><span data-stu-id="1358d-129">Message Service Implementation</span></span>](message-service-implementation.md)

