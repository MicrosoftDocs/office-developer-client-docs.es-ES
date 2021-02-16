---
title: Introducción a los formularios MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4e7d48f6f6a47ce28aa0e1291ccef209b998c18e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432523"
---
# <a name="mapi-forms-overview"></a><span data-ttu-id="6e5d7-103">Introducción a los formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="6e5d7-103">MAPI forms overview</span></span>
  
<span data-ttu-id="6e5d7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e5d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e5d7-105">Un formulario MAPI es un visor de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-105">A MAPI form is a viewer for a message.</span></span> <span data-ttu-id="6e5d7-106">Cada mensaje tiene una clase de mensaje que determina el formulario concreto que se usa como visor.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-106">Every message has a message class that dictates the particular form that is used as its viewer.</span></span> <span data-ttu-id="6e5d7-107">MAPI define varias clases de mensajes y ha implementado los formularios para ver los mensajes de estas clases.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-107">MAPI defines several message classes and has implemented the forms for viewing messages of these classes.</span></span> <span data-ttu-id="6e5d7-108">Los desarrolladores de software cliente pueden crear nuevas clases de mensajes y formularios personalizados para ver los mensajes creados mediante las nuevas clases.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-108">Client software developers can create new message classes and custom forms for viewing messages created by using the new classes.</span></span>
  
<span data-ttu-id="6e5d7-109">Cada formulario personalizado implementa un conjunto de comandos de menú estándar, como **Abrir** **,** Crear **,** Eliminar y **Responder,** y un conjunto de comandos específicos del formulario en particular.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-109">Every custom form implements a set of standard menu commands, such as **Open**, **Create**, **Delete**, and **Reply**, and a set of commands that are specific to the particular form.</span></span> <span data-ttu-id="6e5d7-110">Algunos de los comandos de formulario se integran con la interfaz de usuario de la aplicación cliente cuando el formulario está activo; otros comandos de formulario reemplazan completamente los comandos de cliente.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-110">Some of the form commands are integrated with the user interface of the client application when the form is active; other form commands completely replace the client commands.</span></span> 
  
<span data-ttu-id="6e5d7-111">En la siguiente ilustración se muestra la relación entre los componentes MAPI implicados en el uso de formularios.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-111">The following illustration shows the relationship between the MAPI components involved in using forms.</span></span> 
  
<span data-ttu-id="6e5d7-112">**Arquitectura de formulario MAPI**</span><span class="sxs-lookup"><span data-stu-id="6e5d7-112">**MAPI form architecture**</span></span>
  
<span data-ttu-id="6e5d7-113">![Arquitectura de formulario]MAPI de arquitectura(media/forms01.gif "de formulario MAPI")</span><span class="sxs-lookup"><span data-stu-id="6e5d7-113">![MAPI form architecture](media/forms01.gif "MAPI form architecture")</span></span>
  
<span data-ttu-id="6e5d7-114">En el diagrama, observe que el administrador de formularios desempeña un rol similar a otros proveedores de servicios MAPI, aunque no es un proveedor de servicios en sí.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-114">In the diagram, notice that the form manager plays a role that is similar to other MAPI service providers, although it is not a service provider itself.</span></span> <span data-ttu-id="6e5d7-115">El administrador de formularios es un ARCHIVO DLL reemplazable que implementa algunas de las interfaces MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-115">The form manager is a replaceable DLL that implements some of the MAPI interfaces.</span></span> <span data-ttu-id="6e5d7-116">Aunque los programadores pueden implementar su propio administrador de formularios, la mayoría de los entornos usarán el administrador de formularios proporcionado por Microsoft debido a la complejidad del administrador de formularios.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-116">Although developers can implement their own form manager, most environments will use the form manager provided by Microsoft due to the form manager's complexity.</span></span>
  
<span data-ttu-id="6e5d7-117">En la siguiente lista se describen los componentes del diagrama y su relación con otros componentes:</span><span class="sxs-lookup"><span data-stu-id="6e5d7-117">The following list describes the components in the diagram and their relationship to other components:</span></span>
  
- <span data-ttu-id="6e5d7-118">Cliente de mensajería: una aplicación que puede usar objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-118">Messaging client: An application that can use form objects.</span></span> <span data-ttu-id="6e5d7-119">El cliente de mensajería usa las interfaces de formulario MAPI para comunicarse con el administrador de formularios para cargar mensajes en objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-119">The messaging client uses the MAPI form interfaces to communicate with the form manager to load messages into form objects.</span></span>
    
- <span data-ttu-id="6e5d7-120">Interfaces de formulario MAPI: un estándar definido para la comunicación entre componentes MAPI relacionados con formularios.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-120">MAPI form interfaces: A defined standard for communication between MAPI components that are related to forms.</span></span>
    
- <span data-ttu-id="6e5d7-121">Administrador de formularios: dll que los clientes de mensajería usan para controlar la instalación de formularios en bibliotecas de formularios, la carga de servidores de formularios y la comunicación inicial entre clientes de mensajería y servidores de formularios.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-121">Form manager: The DLL that messaging clients use to handle installation of forms in form libraries, loading of form servers, and initial communication between messaging clients and form servers.</span></span>
    
- <span data-ttu-id="6e5d7-122">Bibliotecas de formularios: almacenamiento permanente para los archivos ejecutables asociados con servidores de formulario.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-122">Form libraries: Permanent storage for the executable files associated with form servers.</span></span>
    
- <span data-ttu-id="6e5d7-123">Servidores de formulario: archivos ejecutables que implementan un formulario.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-123">Form servers: Executable files that implement a form.</span></span> <span data-ttu-id="6e5d7-124">Los servidores de formularios crean objetos de formulario e interfaces de usuario para tratar mensajes específicos.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-124">Form servers create form objects and user interfaces to deal with specific messages.</span></span> <span data-ttu-id="6e5d7-125">Este ejecutable también es un servidor OLE y se adhiere a las convenciones OLE habituales.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-125">This executable is also an OLE server and adheres to the usual OLE conventions.</span></span>
    
- <span data-ttu-id="6e5d7-126">Objetos de formulario: objetos en tiempo de ejecución creados por servidores de formulario que corresponden a mensajes específicos.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-126">Form objects: Run-time objects created by form servers that correspond to specific messages.</span></span> <span data-ttu-id="6e5d7-127">Los objetos de formulario se ejecutan en el mismo contexto de proceso que su servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-127">Form objects run in the same process context as their form server.</span></span>
    
<span data-ttu-id="6e5d7-128">Para obtener más información acerca de los componentes de formulario MAPI, vea [Formularios MAPI](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="6e5d7-128">For more information about MAPI form components, see [MAPI Forms](mapi-forms.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e5d7-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6e5d7-129">See also</span></span>

- [<span data-ttu-id="6e5d7-130">Arquitectura y características mapi</span><span class="sxs-lookup"><span data-stu-id="6e5d7-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

