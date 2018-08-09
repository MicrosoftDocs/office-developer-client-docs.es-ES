---
title: Admitir la instalación del servicio de mensajería
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bf3e79ad32801a659df2c68016167d3b547ddc6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820799"
---
# <a name="supporting-message-service-installation"></a><span data-ttu-id="adb6a-103">Admitir la instalación del servicio de mensajería</span><span class="sxs-lookup"><span data-stu-id="adb6a-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="adb6a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="adb6a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="adb6a-105">El programa de instalación para instalar el servicio de mensajes debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="adb6a-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="adb6a-106">Copie los archivos de servicio de mensajes, como el servicio de mensajes y el proveedor de servicios de archivos DLL, desde un CD o disco, en una unidad local en la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="adb6a-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="adb6a-107">Los archivos que deben copiarse dependen de su servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="adb6a-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="adb6a-108">Normalmente se copie al menos una DLL.</span><span class="sxs-lookup"><span data-stu-id="adb6a-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="adb6a-109">Agregar entradas al archivo de configuración Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="adb6a-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="adb6a-110">Para obtener más información acerca de cómo modificar este archivo para admitir los proveedores de servicios en el servicio de mensajes, vea [Formato de archivo de MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="adb6a-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="adb6a-111">Agregar entradas, según corresponda, en el registro del sistema para servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="adb6a-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="adb6a-112">Para obtener más información acerca de cómo deben aparecer las entradas en el registro del sistema, vea [instalar el subsistema MAPI](installing-the-mapi-subsystem.md).</span><span class="sxs-lookup"><span data-stu-id="adb6a-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="adb6a-113">Crear un perfil predeterminado si no existe todavía mediante uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="adb6a-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="adb6a-114">El Asistente para perfiles para crear un perfil mediante el uso de interacción del usuario a través de una serie de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="adb6a-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="adb6a-115">Para obtener más información acerca de cómo utilizar al Asistente para perfiles, vea [creación de un perfil mediante el Asistente para perfiles](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="adb6a-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="adb6a-116">El Panel de Control para crear un perfil mediante el uso de interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="adb6a-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="adb6a-117">El Panel de Control ofrece al usuario más flexibilidad que el Asistente para perfiles para configurar los servicios de mensaje y establecer las propiedades de perfil.</span><span class="sxs-lookup"><span data-stu-id="adb6a-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="adb6a-118">Colocar el programa de instalación en un directorio público designado.</span><span class="sxs-lookup"><span data-stu-id="adb6a-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="adb6a-119">Esto es importante porque la mayoría de los clientes de configuración, como el Panel de Control, requieren que los usuarios escribir el nombre del directorio.</span><span class="sxs-lookup"><span data-stu-id="adb6a-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="adb6a-120">El Panel de Control invoca un programa de instalación cuando un usuario hace clic en el botón **Agregar** , invoca el cuadro de diálogo **Utilizar disco** y especifica la ruta de acceso al programa.</span><span class="sxs-lookup"><span data-stu-id="adb6a-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="adb6a-121">El Panel de Control se ejecuta el programa y llama a la función de punto de entrada del servicio de su mensaje con el parámetro _ulContext_ establecido en MSG_SERVICE_INSTALL.</span><span class="sxs-lookup"><span data-stu-id="adb6a-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="adb6a-122">Dado que los perfiles son un elemento prescindibles de la arquitectura MAPI, asegúrese de que el programa de instalación no almacenar nada en el perfil predeterminado que sería difícil de volver a crear.</span><span class="sxs-lookup"><span data-stu-id="adb6a-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="adb6a-123">No hay ningún utilidades para la recuperación de perfil, para mover los perfiles de un equipo a otro, de copia de seguridad sin conexión o para la restauración individual o global de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="adb6a-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="adb6a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="adb6a-124">See also</span></span>



[<span data-ttu-id="adb6a-125">Implementación de servicios de mensajería</span><span class="sxs-lookup"><span data-stu-id="adb6a-125">Message Service Implementation</span></span>](message-service-implementation.md)

