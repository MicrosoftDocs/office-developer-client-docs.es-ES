---
title: Admitir la configuración del servicio de soporte mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: aa1a433e90eda24f1199783bc604e047deb03ecd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418998"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="f3899-103">Admitir la configuración del servicio de soporte mensaje</span><span class="sxs-lookup"><span data-stu-id="f3899-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="f3899-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3899-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3899-105">Para admitir la configuración del servicio de mensajes, use el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="f3899-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="f3899-106">Implementar una función de punto de entrada que se ajuste al prototipo [MSGSERVICEENTRY.](msgserviceentry.md)</span><span class="sxs-lookup"><span data-stu-id="f3899-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="f3899-107">Las funciones de punto de entrada del servicio de mensajes administran el acceso a los datos de configuración y se les llama en las siguientes circunstancias:</span><span class="sxs-lookup"><span data-stu-id="f3899-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="f3899-108">Cuando un cliente inicia sesión para recuperar información para configurar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f3899-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="f3899-109">Cuando un cliente desea ver o cambiar una propiedad de configuración.</span><span class="sxs-lookup"><span data-stu-id="f3899-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="f3899-110">Aunque la mayoría de los servicios de mensajes proporcionarán funciones de punto de entrada, como deberían, estas funciones no son estrictamente necesarias.</span><span class="sxs-lookup"><span data-stu-id="f3899-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="f3899-111">Los servicios de mensajes pueden proporcionar acceso a los datos de configuración de otras maneras.</span><span class="sxs-lookup"><span data-stu-id="f3899-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="f3899-112">Sin embargo, el uso de una función de punto de entrada estandariza y simplifica el proceso de configuración.</span><span class="sxs-lookup"><span data-stu-id="f3899-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="f3899-113">MAPI espera que todas las funciones de punto de entrada del servicio de mensajes puedan almacenar y recuperar propiedades de las secciones de perfil asociadas a su servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f3899-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="f3899-114">Puede admitir esta funcionalidad de forma interactiva, mediante programación o tanto de forma interactiva como mediante programación.</span><span class="sxs-lookup"><span data-stu-id="f3899-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="f3899-115">Para admitir la configuración interactiva, proporcione una hoja de propiedades que muestre las propiedades implicadas en la configuración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f3899-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="f3899-116">Como opción, también puede proporcionar hojas de propiedades para cada proveedor configurable.</span><span class="sxs-lookup"><span data-stu-id="f3899-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="f3899-117">Algunos servicios de mensajes restringen a los usuarios a una vista de solo lectura de las propiedades de configuración; otros servicios de mensajes permiten a los usuarios realizar cambios.</span><span class="sxs-lookup"><span data-stu-id="f3899-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="f3899-118">Para admitir la configuración mediante programación, la función de punto de entrada del servicio de mensajes debe poder funcionar sin la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="f3899-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="f3899-119">Si el Asistente para perfiles puede llamar al servicio de mensajes, debe admitir la configuración mediante programación.</span><span class="sxs-lookup"><span data-stu-id="f3899-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="f3899-120">Si el servicio de mensajes no se permite configurar mediante el Asistente para perfiles, puede elegir si desea admitir o no la configuración mediante programación.</span><span class="sxs-lookup"><span data-stu-id="f3899-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="f3899-121">Para obtener más información acerca de cómo admitir la configuración en una función de punto de entrada del servicio de mensajes, vea [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="f3899-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="f3899-122">Publique el nombre de la función de punto de entrada del servicio de mensajes en el archivo de configuración Mapisvc.inf incluyendo la siguiente entrada en la sección de servicio de mensajes:</span><span class="sxs-lookup"><span data-stu-id="f3899-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="f3899-123">Cree uno o más cuadros de diálogo de hoja de propiedades para mostrar los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="f3899-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="f3899-124">Realice las siguientes tareas si desea permitir que el Asistente para perfiles configure el servicio de mensajes:</span><span class="sxs-lookup"><span data-stu-id="f3899-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="f3899-125">Implementar una función de punto de entrada que se ajuste al prototipo [WIZARDENTRY.](wizardentry.md)</span><span class="sxs-lookup"><span data-stu-id="f3899-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="f3899-126">Implemente un procedimiento de cuadro de diálogo estándar de Windows que se ajuste al prototipo [SERVICEWIZARDDLGPROC.](servicewizarddlgproc.md)</span><span class="sxs-lookup"><span data-stu-id="f3899-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="f3899-127">Mejore la función de punto de entrada del servicio de mensajes para responder a eventos adicionales.</span><span class="sxs-lookup"><span data-stu-id="f3899-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3899-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f3899-128">See also</span></span>

- [<span data-ttu-id="f3899-129">Implementación del servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="f3899-129">Message Service Implementation</span></span>](message-service-implementation.md)

