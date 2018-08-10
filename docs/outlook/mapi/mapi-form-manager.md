---
title: Administrador de formularios MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d12d879ea5a82c5e0e3978d90694b3851aaac5cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818114"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="6576e-103">Administrador de formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="6576e-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="6576e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6576e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6576e-105">El Administrador de un formulario es un objeto que implementa la interfaz [IMAPIFormMgr](imapiformmgriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="6576e-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="6576e-106">La mayoría de las organizaciones utilizará el Administrador de formulario que se proporciona con MAPI, que se conoce como el Administrador de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6576e-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="6576e-107">Sin embargo, una organización puede reemplazar el Administrador de formulario predeterminado con el Administrador de un formulario personalizado, si así lo desea.</span><span class="sxs-lookup"><span data-stu-id="6576e-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="6576e-108">El Administrador de formulario se encarga de localizar formularios dentro de las bibliotecas de formularios, carga de los formularios en respuesta a las solicitudes de usuario e instalar formularios en la biblioteca de formularios local, biblioteca de formularios de carpeta o biblioteca de formularios personales de un usuario.</span><span class="sxs-lookup"><span data-stu-id="6576e-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="6576e-109">Para un usuario interactuar con un mensaje, una instancia del servidor de formulario para la clase de mensaje del mensaje debe ser creada y activada para mostrar el mensaje y realizar la operación solicitada en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6576e-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="6576e-110">Tal como se describe en el tema de [Las bibliotecas de formularios de MAPI](mapi-form-libraries.md), la implementación de un formulario puede existir en varias ubicaciones diferentes (bibliotecas de formularios) y no hay ninguna garantía de que un formulario o en su servidor va a estar disponible localmente o en una ejecución de estado cuando un usuario desea interactuar con él.</span><span class="sxs-lookup"><span data-stu-id="6576e-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="6576e-111">El Administrador de formulario se encarga de los detalles de localizar y activar el formulario.</span><span class="sxs-lookup"><span data-stu-id="6576e-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="6576e-112">Los clientes usan los servicios proporcionados por el Administrador de formularios para encontrar y activar formularios.</span><span class="sxs-lookup"><span data-stu-id="6576e-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="6576e-113">La interfaz de **IMAPIFormMgr** se implementa mediante el Administrador de formulario y se llama por los clientes para tener acceso a sus servicios.</span><span class="sxs-lookup"><span data-stu-id="6576e-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="6576e-114">El Administrador de formulario es un componente esencial porque oculta casi todos los detalles de búsqueda y activación de los formularios de clientes de mensajería.</span><span class="sxs-lookup"><span data-stu-id="6576e-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="6576e-115">Al cargar los servidores de formulario, el Administrador de formulario predeterminado carga el formulario desde la primera biblioteca de formularios en la que se encuentra una implementación para la clase de mensaje del formulario.</span><span class="sxs-lookup"><span data-stu-id="6576e-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="6576e-116">El Administrador de formulario predeterminado busca las bibliotecas de formularios en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="6576e-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="6576e-117">Biblioteca de formulario local del usuario.</span><span class="sxs-lookup"><span data-stu-id="6576e-117">The user's local form library.</span></span> <span data-ttu-id="6576e-118">Esta biblioteca de formularios se busca en primer lugar porque proporciona el acceso más rápido a la implementación de un formulario si la implementación está instalada en la biblioteca de formularios local.</span><span class="sxs-lookup"><span data-stu-id="6576e-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="6576e-119">La biblioteca de formularios de la carpeta de contenedor del mensaje: la carpeta en la que está almacenado el mensaje que se está cargando.</span><span class="sxs-lookup"><span data-stu-id="6576e-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="6576e-120">Biblioteca de formularios personal del usuario.</span><span class="sxs-lookup"><span data-stu-id="6576e-120">The user's personal form library.</span></span>
    
<span data-ttu-id="6576e-121">El Administrador de un formulario personalizado puede buscar las bibliotecas de formulario disponibles en cualquier orden, o puede implementar otras bibliotecas de formularios, como una biblioteca de formularios de toda la organización.</span><span class="sxs-lookup"><span data-stu-id="6576e-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="6576e-122">Para obtener más detalles sobre las bibliotecas de formularios, vea [Bibliotecas de formularios de MAPI](mapi-form-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="6576e-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6576e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6576e-123">See also</span></span>



[<span data-ttu-id="6576e-124">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="6576e-124">MAPI Forms</span></span>](mapi-forms.md)

