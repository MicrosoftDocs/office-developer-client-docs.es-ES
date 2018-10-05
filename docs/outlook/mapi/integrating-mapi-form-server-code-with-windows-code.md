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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397866"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="d3c9a-103">Integración de código de servidor de formulario MAPI con código de Windows</span><span class="sxs-lookup"><span data-stu-id="d3c9a-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="d3c9a-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3c9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3c9a-105">Recuerde que el servidor de formulario es una aplicación de Win32.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="d3c9a-106">Por lo tanto, hay algunas tareas relacionadas con la carga de su servidor de formulario en la memoria y salir sin problemas.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="d3c9a-107">Al igual que todas las aplicaciones de Windows, el punto de entrada para el servidor de formulario es la función **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="d3c9a-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="d3c9a-108">Esta función es el lugar adecuado para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="d3c9a-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="d3c9a-109">Crear y registrar una clase de ventana para que su servidor de formulario puede interactuar con otros componentes OLE.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="d3c9a-110">Crear y registrar una clase de ventana o las clases para las interfaces de usuario de los objetos del formulario.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="d3c9a-111">Llamar a la función de [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="d3c9a-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="d3c9a-112">**MAPIInitialize** administra la OLE inicialización necesaria para usted, así como.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="d3c9a-113">Debe realizarse una vez por cada instancia de su servidor del formulario.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="d3c9a-114">Registrar un atom global con una representación de cadena del identificador de clase (CLSID) del servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="d3c9a-115">Este atom debería haber por la duración del servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="d3c9a-116">Llamar a la función OLE [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) para registrar el generador de clases del servidor de su formulario con OLE.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-116">Calling the OLE function [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="d3c9a-117">Creación de una ventana principal para recibir los mensajes.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="d3c9a-118">Probablemente esta ventana no necesita ser visible, ya que el usuario interactúa con la versión de windows asociados con los objetos de formulario individuales.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="d3c9a-119">Sin embargo, durante el desarrollo, la ventana principal de puede ser un lugar adecuado para la depuración de salida o el control de su servidor del formulario.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="d3c9a-120">Creación de un bucle de mensajes que se ejecuta para la duración del servidor de formulario, traducir y enviar mensajes de windows a los objetos del formulario activo.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="d3c9a-121">Cuando sale de su servidor de formulario, debe realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="d3c9a-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="d3c9a-122">Llame a la función OLE [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) para revocar el registro OLE de la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-122">Call the OLE function [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="d3c9a-123">Llamar a **MAPIUninitialize** para cerrar correctamente la conexión del servidor de formulario a MAPI.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="d3c9a-124">Eliminar el atom global que contiene la representación de cadena del identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3c9a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3c9a-125">See also</span></span>



[<span data-ttu-id="d3c9a-126">Escribir código de servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="d3c9a-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

