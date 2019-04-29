---
title: Compatibilidad con la instalación del servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 328884e8758e679eb1c9d968547cba02c01d4d47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404704"
---
# <a name="supporting-message-service-installation"></a><span data-ttu-id="81ffa-103">Compatibilidad con la instalación del servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="81ffa-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="81ffa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81ffa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81ffa-105">El programa de instalación para instalar el servicio de mensajes debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="81ffa-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="81ffa-106">Copie los archivos del servicio de mensajes, como las DLL del servicio de mensajes y del proveedor de servicios, desde un CD o un disco a una unidad local de la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="81ffa-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="81ffa-107">Los archivos que deben copiarse dependen de su servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="81ffa-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="81ffa-108">Normalmente, copiará al menos una DLL.</span><span class="sxs-lookup"><span data-stu-id="81ffa-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="81ffa-109">Agregue entradas al archivo de configuración MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="81ffa-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="81ffa-110">Para obtener más información acerca de cómo modificar este archivo para que admita los proveedores de servicios en el servicio de mensajes, vea el [formato de archivo de MapiSvc. inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="81ffa-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="81ffa-111">Agregue entradas, según corresponda, al registro del sistema para los servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="81ffa-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="81ffa-112">Para obtener más información acerca de cómo deben aparecer las entradas en el registro del sistema, vea [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span><span class="sxs-lookup"><span data-stu-id="81ffa-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="81ffa-113">Cree un perfil predeterminado si todavía no existe con uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="81ffa-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="81ffa-114">El Asistente para perfiles para crear un perfil mediante la interacción del usuario a través de una serie de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="81ffa-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="81ffa-115">Para obtener más información acerca del uso del Asistente para perfiles, consulte [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="81ffa-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="81ffa-116">Panel de control para crear un perfil mediante la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="81ffa-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="81ffa-117">El panel de control ofrece al usuario más flexibilidad que el Asistente para perfiles para configurar los servicios de mensajes y establecer las propiedades de perfil.</span><span class="sxs-lookup"><span data-stu-id="81ffa-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="81ffa-118">Ponga el programa de instalación en un directorio público designado.</span><span class="sxs-lookup"><span data-stu-id="81ffa-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="81ffa-119">Esto es importante porque la mayoría de los clientes de configuración, como el panel de control, requieren que los usuarios escriban el nombre del directorio.</span><span class="sxs-lookup"><span data-stu-id="81ffa-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="81ffa-120">El panel de control invoca un programa de instalación cuando un usuario hace clic en el botón **Agregar** , invoca el cuadro de diálogo **utilizar disco** y especifica la ruta de acceso al programa.</span><span class="sxs-lookup"><span data-stu-id="81ffa-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="81ffa-121">El panel de control ejecuta el programa y llama a la función de punto de entrada del servicio de mensajes con el parámetro _ulContext_ establecido en MSG_SERVICE_INSTALL.</span><span class="sxs-lookup"><span data-stu-id="81ffa-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="81ffa-122">Debido a que los perfiles son una parte que puede pasarse de la arquitectura MAPI, asegúrese de que el programa de instalación no almacena nada en el perfil predeterminado que sería difícil de volver a crear.</span><span class="sxs-lookup"><span data-stu-id="81ffa-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="81ffa-123">No existen utilidades para la recuperación de perfiles, para mover perfiles de un equipo a otro, para copias de seguridad sin conexión o para restauración individual o global a partir de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="81ffa-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81ffa-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="81ffa-124">See also</span></span>



[<span data-ttu-id="81ffa-125">Implementación del servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="81ffa-125">Message Service Implementation</span></span>](message-service-implementation.md)

