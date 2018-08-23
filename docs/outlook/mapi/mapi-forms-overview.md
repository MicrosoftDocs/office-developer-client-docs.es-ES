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
ms.openlocfilehash: 29132f24547dc744efcd6f2b6e4a8f6af87ab53c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574415"
---
# <a name="mapi-forms-overview"></a><span data-ttu-id="6c112-103">Introducción a los formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="6c112-103">MAPI forms overview</span></span>
  
<span data-ttu-id="6c112-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c112-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c112-105">Un formulario MAPI es un visor para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="6c112-105">A MAPI form is a viewer for a message.</span></span> <span data-ttu-id="6c112-106">Cada mensaje tiene una clase de mensaje que determina la forma concreta que se usa como su visor.</span><span class="sxs-lookup"><span data-stu-id="6c112-106">Every message has a message class that dictates the particular form that is used as its viewer.</span></span> <span data-ttu-id="6c112-107">MAPI define varias clases de mensaje y ha implementado los formularios para ver los mensajes de estas clases.</span><span class="sxs-lookup"><span data-stu-id="6c112-107">MAPI defines several message classes and has implemented the forms for viewing messages of these classes.</span></span> <span data-ttu-id="6c112-108">Los programadores de software de cliente pueden crear nuevas clases de mensaje y formularios personalizados para la visualización de los mensajes creados mediante el uso de las clases nuevas.</span><span class="sxs-lookup"><span data-stu-id="6c112-108">Client software developers can create new message classes and custom forms for viewing messages created by using the new classes.</span></span>
  
<span data-ttu-id="6c112-109">Cada formulario personalizado implementa un conjunto de comandos del menú estándar, como **Abrir**, **crear**, **Eliminar**y **respuesta**y un conjunto de comandos que son específicos de la forma concreta.</span><span class="sxs-lookup"><span data-stu-id="6c112-109">Every custom form implements a set of standard menu commands, such as **Open**, **Create**, **Delete**, and **Reply**, and a set of commands that are specific to the particular form.</span></span> <span data-ttu-id="6c112-110">Algunos de los comandos de formulario se integran con la interfaz de usuario de la aplicación cliente cuando el formulario está activo; otros comandos de formulario reemplazan completamente los comandos de cliente.</span><span class="sxs-lookup"><span data-stu-id="6c112-110">Some of the form commands are integrated with the user interface of the client application when the form is active; other form commands completely replace the client commands.</span></span> 
  
<span data-ttu-id="6c112-111">En la siguiente ilustración se muestra la relación entre los componentes MAPI relacionados con el uso de formularios.</span><span class="sxs-lookup"><span data-stu-id="6c112-111">The following illustration shows the relationship between the MAPI components involved in using forms.</span></span> 
  
<span data-ttu-id="6c112-112">**Arquitectura de formulario MAPI**</span><span class="sxs-lookup"><span data-stu-id="6c112-112">**MAPI form architecture**</span></span>
  
<span data-ttu-id="6c112-113">![Arquitectura de formulario MAPI] (media/forms01.gif "Arquitectura de formulario MAPI")</span><span class="sxs-lookup"><span data-stu-id="6c112-113">![MAPI form architecture](media/forms01.gif "MAPI form architecture")</span></span>
  
<span data-ttu-id="6c112-114">En el diagrama, tenga en cuenta que el Administrador de formulario desempeña un papel que es similar a otros proveedores de servicios MAPI, aunque no es un proveedor de servicios de sí mismo.</span><span class="sxs-lookup"><span data-stu-id="6c112-114">In the diagram, notice that the form manager plays a role that is similar to other MAPI service providers, although it is not a service provider itself.</span></span> <span data-ttu-id="6c112-115">El Administrador de formulario es un archivo DLL reemplazable que implementa algunas de las interfaces MAPI.</span><span class="sxs-lookup"><span data-stu-id="6c112-115">The form manager is a replaceable DLL that implements some of the MAPI interfaces.</span></span> <span data-ttu-id="6c112-116">Aunque los desarrolladores pueden implementar su propio administrador de formularios, mayoría de los entornos utilizará el Administrador de formulario proporcionado por Microsoft debido a la complejidad del director de formulario.</span><span class="sxs-lookup"><span data-stu-id="6c112-116">Although developers can implement their own form manager, most environments will use the form manager provided by Microsoft due to the form manager's complexity.</span></span>
  
<span data-ttu-id="6c112-117">En la siguiente lista se describe los componentes en el diagrama y su relación con otros componentes:</span><span class="sxs-lookup"><span data-stu-id="6c112-117">The following list describes the components in the diagram and their relationship to other components:</span></span>
  
- <span data-ttu-id="6c112-118">Cliente de mensajería: una aplicación que puede usar objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="6c112-118">Messaging client: An application that can use form objects.</span></span> <span data-ttu-id="6c112-119">El cliente de mensajería usa las interfaces de formulario MAPI para comunicarse con el Administrador de formulario para cargar los mensajes en los objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="6c112-119">The messaging client uses the MAPI form interfaces to communicate with the form manager to load messages into form objects.</span></span>
    
- <span data-ttu-id="6c112-120">Interfaces de formulario MAPI: un estándar definido para la comunicación entre los componentes MAPI que están relacionadas con los formularios.</span><span class="sxs-lookup"><span data-stu-id="6c112-120">MAPI form interfaces: A defined standard for communication between MAPI components that are related to forms.</span></span>
    
- <span data-ttu-id="6c112-121">Administrador de formularios: el archivo DLL que usan los clientes de mensajería para controlar la instalación de los formularios en las bibliotecas de formularios, la carga de los servidores de formulario y la comunicación inicial entre clientes de mensajería y los servidores de formulario.</span><span class="sxs-lookup"><span data-stu-id="6c112-121">Form manager: The DLL that messaging clients use to handle installation of forms in form libraries, loading of form servers, and initial communication between messaging clients and form servers.</span></span>
    
- <span data-ttu-id="6c112-122">Bibliotecas de formularios: ubicación de almacenamiento permanente para los archivos ejecutables asociados con los servidores de formulario.</span><span class="sxs-lookup"><span data-stu-id="6c112-122">Form libraries: Permanent storage for the executable files associated with form servers.</span></span>
    
- <span data-ttu-id="6c112-123">Servidores de formulario: archivos ejecutables que implementan un formulario.</span><span class="sxs-lookup"><span data-stu-id="6c112-123">Form servers: Executable files that implement a form.</span></span> <span data-ttu-id="6c112-124">Servidores de formulario crean objetos de formulario e interfaces de usuario para abordar los problemas con mensajes específicos.</span><span class="sxs-lookup"><span data-stu-id="6c112-124">Form servers create form objects and user interfaces to deal with specific messages.</span></span> <span data-ttu-id="6c112-125">Este archivo ejecutable también es un servidor OLE y sigue las convenciones usuales de OLE.</span><span class="sxs-lookup"><span data-stu-id="6c112-125">This executable is also an OLE server and adheres to the usual OLE conventions.</span></span>
    
- <span data-ttu-id="6c112-126">Objetos de formulario: objetos de tiempo de ejecución creados por los servidores de formulario que se corresponden con mensajes específicos.</span><span class="sxs-lookup"><span data-stu-id="6c112-126">Form objects: Run-time objects created by form servers that correspond to specific messages.</span></span> <span data-ttu-id="6c112-127">Objetos de formulario se ejecuten en el mismo contexto de proceso como su servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="6c112-127">Form objects run in the same process context as their form server.</span></span>
    
<span data-ttu-id="6c112-128">Para obtener más información acerca de los componentes de formulario MAPI, vea [Los formularios MAPI](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="6c112-128">For more information about MAPI form components, see [MAPI Forms](mapi-forms.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6c112-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6c112-129">See also</span></span>

- [<span data-ttu-id="6c112-130">Arquitectura y las características MAPI</span><span class="sxs-lookup"><span data-stu-id="6c112-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

