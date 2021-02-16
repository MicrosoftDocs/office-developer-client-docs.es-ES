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
ms.openlocfilehash: 3059183103ca2552505486b5ec54366729ae4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430199"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="dd474-103">Administrador de formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="dd474-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="dd474-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd474-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd474-105">Un administrador de formularios es un objeto que implementa la [interfaz IMAPIFormMgr.](imapiformmgriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="dd474-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="dd474-106">La mayoría de las organizaciones usarán el administrador de formularios suministrado con MAPI, conocido como administrador de formularios predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dd474-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="dd474-107">Sin embargo, una organización puede reemplazar el administrador de formularios predeterminado por un administrador de formularios personalizado si lo desea.</span><span class="sxs-lookup"><span data-stu-id="dd474-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="dd474-108">El administrador de formularios se encarga de buscar formularios en bibliotecas de formularios, cargar formularios en respuesta a solicitudes de usuario e instalar formularios en la biblioteca de formularios local, biblioteca de formularios de carpetas o biblioteca de formularios personal de un usuario.</span><span class="sxs-lookup"><span data-stu-id="dd474-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="dd474-109">Para que un usuario interactúe con un mensaje, se debe crear y activar una instancia del servidor de formulario para la clase de mensaje del mensaje para mostrar el mensaje y llevar a cabo la operación solicitada en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd474-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="dd474-110">Como se describe en el tema Bibliotecas de [formularios MAPI,](mapi-form-libraries.md)la implementación de un formulario puede existir en varias ubicaciones diferentes (bibliotecas de formularios) y no hay ninguna garantía de que un formulario o su servidor estarán disponibles localmente o en un estado en ejecución cuando un usuario desea interactuar con él.</span><span class="sxs-lookup"><span data-stu-id="dd474-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="dd474-111">El administrador de formularios se encarga de los detalles de la localización y activación del formulario.</span><span class="sxs-lookup"><span data-stu-id="dd474-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="dd474-112">Los clientes usan servicios proporcionados por el administrador de formularios para buscar y activar formularios.</span><span class="sxs-lookup"><span data-stu-id="dd474-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="dd474-113">El administrador de formularios implementa la interfaz **IMAPIFormMgr** y los clientes los llaman para obtener acceso a sus servicios.</span><span class="sxs-lookup"><span data-stu-id="dd474-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="dd474-114">El administrador de formularios es un componente esencial porque oculta casi todos los detalles de la búsqueda y activación de formularios de clientes de mensajería.</span><span class="sxs-lookup"><span data-stu-id="dd474-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="dd474-115">Al cargar servidores de formulario, el administrador de formularios predeterminado carga el formulario desde la primera biblioteca de formularios en la que se encuentra una implementación para la clase de mensaje del formulario.</span><span class="sxs-lookup"><span data-stu-id="dd474-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="dd474-116">El administrador de formularios predeterminado busca en las bibliotecas de formularios en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="dd474-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="dd474-117">Biblioteca de formularios local del usuario.</span><span class="sxs-lookup"><span data-stu-id="dd474-117">The user's local form library.</span></span> <span data-ttu-id="dd474-118">Esta biblioteca de formularios se busca primero porque proporciona el acceso más rápido a la implementación de un formulario si la implementación está instalada en la biblioteca de formularios local.</span><span class="sxs-lookup"><span data-stu-id="dd474-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="dd474-119">La biblioteca de formularios de carpeta del contenedor del mensaje: la carpeta en la que se almacena el mensaje que se está cargando.</span><span class="sxs-lookup"><span data-stu-id="dd474-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="dd474-120">Biblioteca de formularios personal del usuario.</span><span class="sxs-lookup"><span data-stu-id="dd474-120">The user's personal form library.</span></span>
    
<span data-ttu-id="dd474-121">Un administrador de formularios personalizado puede buscar en las bibliotecas de formularios disponibles en cualquier orden o puede implementar otras bibliotecas de formularios, como una biblioteca de formularios en toda la organización.</span><span class="sxs-lookup"><span data-stu-id="dd474-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="dd474-122">Para obtener más información sobre las bibliotecas de formularios, vea [Bibliotecas de formularios MAPI](mapi-form-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="dd474-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dd474-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dd474-123">See also</span></span>



[<span data-ttu-id="dd474-124">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="dd474-124">MAPI Forms</span></span>](mapi-forms.md)

