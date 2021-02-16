---
title: Integración de código de servidor de formulario MAPI con código de Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332182"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="c0b2d-103">Integración de código de servidor de formulario MAPI con código de Windows</span><span class="sxs-lookup"><span data-stu-id="c0b2d-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="c0b2d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0b2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0b2d-105">Recuerde que el servidor de formulario es una aplicación win32.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="c0b2d-106">Como tal, hay algunas tareas relacionadas con la carga del servidor de formularios en la memoria y la salida limpia.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="c0b2d-107">Al igual que todas las aplicaciones de Windows, el punto de entrada del servidor de formulario es la **función WinMain.**</span><span class="sxs-lookup"><span data-stu-id="c0b2d-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="c0b2d-108">Esta función es el lugar adecuado para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="c0b2d-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="c0b2d-109">Crear y registrar una clase de ventana para que el servidor de formularios pueda interactuar con otros componentes OLE.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="c0b2d-110">Crear y registrar una clase o clases de ventana para las interfaces de usuario de los objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="c0b2d-111">Llamar a [la función MAPIInitialize.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="c0b2d-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="c0b2d-112">**MAPIInitialize también** controla la inicialización OLE necesaria.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="c0b2d-113">Esto debe hacerse una vez por instancia del servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="c0b2d-114">Registrar un atom global con una representación de cadena del identificador de clase (CLSID) del servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="c0b2d-115">Este atom debe existir durante la duración del servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="c0b2d-116">Llamar a la función OLE [CoRegisterClassObject para](https://msdn.microsoft.com/library/ms693407.aspx) registrar la fábrica de clases del servidor de formulario con OLE.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-116">Calling the OLE function [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="c0b2d-117">Crear una ventana principal para recibir mensajes.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="c0b2d-118">Es probable que esta ventana no tenga que estar visible porque el usuario interactuará con las ventanas específicas asociadas con objetos de formulario individuales.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="c0b2d-119">Sin embargo, durante el desarrollo, la ventana principal puede ser un lugar conveniente para depurar los resultados o el control del servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="c0b2d-120">Creación de un bucle de mensajes que se ejecuta durante el ciclo de vida del servidor de formularios, traduciendo y distribuyendo mensajes de Windows a objetos de formulario activos.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="c0b2d-121">Cuando el servidor de formulario se cierra, debe realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="c0b2d-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="c0b2d-122">Llame a la función OLE [CoRevokeClassObject para](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) revocar el registro OLE de la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-122">Call the OLE function [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="c0b2d-123">Llame **a MAPIUninitialize** para cerrar correctamente la conexión del servidor de formulario a MAPI.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="c0b2d-124">Elimine el atom global que contiene la representación de cadena del identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="c0b2d-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0b2d-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c0b2d-125">See also</span></span>



[<span data-ttu-id="c0b2d-126">Escritura de código de servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="c0b2d-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

