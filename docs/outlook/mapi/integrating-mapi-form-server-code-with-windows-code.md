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
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="79ce0-103">Integración de código de servidor de formulario MAPI con código de Windows</span><span class="sxs-lookup"><span data-stu-id="79ce0-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="79ce0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79ce0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79ce0-105">Recuerde que el servidor de formularios es una aplicación Win32.</span><span class="sxs-lookup"><span data-stu-id="79ce0-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="79ce0-106">Por lo tanto, hay algunas tareas relacionadas con la carga del servidor de formularios en la memoria y la salida limpia.</span><span class="sxs-lookup"><span data-stu-id="79ce0-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="79ce0-107">Como todas las aplicaciones para Windows, el punto de entrada del servidor de formularios es la función **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="79ce0-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="79ce0-108">Esta función es el punto adecuado para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="79ce0-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="79ce0-109">Crear y registrar una clase de ventana para que el servidor de formularios pueda interactuar con otros componentes OLE.</span><span class="sxs-lookup"><span data-stu-id="79ce0-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="79ce0-110">Crear y registrar una clase o clases de ventana para las interfaces de usuario de los objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="79ce0-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="79ce0-111">Llamar a la función [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="79ce0-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="79ce0-112">**MAPIInitialize** también controla la inicialización OLE necesaria.</span><span class="sxs-lookup"><span data-stu-id="79ce0-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="79ce0-113">Esto debe realizarse una vez por instancia del servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="79ce0-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="79ce0-114">Registrar un átomo global con una representación de cadena del identificador de clase (CLSID) del servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="79ce0-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="79ce0-115">Este átomo debería existir mientras dure el servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="79ce0-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="79ce0-116">Llamar a la función OLE [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) para registrar el generador de clases del servidor de formularios con OLE.</span><span class="sxs-lookup"><span data-stu-id="79ce0-116">Calling the OLE function [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="79ce0-117">Crear una ventana principal para recibir mensajes.</span><span class="sxs-lookup"><span data-stu-id="79ce0-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="79ce0-118">Es probable que esta ventana no necesite ser visible porque el usuario va a interactuar con las ventanas específicas asociadas con los objetos de formulario individuales.</span><span class="sxs-lookup"><span data-stu-id="79ce0-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="79ce0-119">Sin embargo, durante el desarrollo, la ventana principal puede ser un punto útil para depurar el resultado o el control del servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="79ce0-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="79ce0-120">Crear un bucle de mensajes que se ejecute durante el período de duración del servidor de formularios, convirtiendo y distribuyendo mensajes de Windows en objetos de formulario activos.</span><span class="sxs-lookup"><span data-stu-id="79ce0-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="79ce0-121">Cuando se cierre el servidor de formularios, debe realizar las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="79ce0-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="79ce0-122">Llame a la función OLE [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) para revocar el registro OLE de la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="79ce0-122">Call the OLE function [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="79ce0-123">Llame a **MAPIUninitialize** para cerrar correctamente la conexión del servidor de formularios con MAPI.</span><span class="sxs-lookup"><span data-stu-id="79ce0-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="79ce0-124">Elimine el átomo global que contiene la representación de cadena del identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="79ce0-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79ce0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="79ce0-125">See also</span></span>



[<span data-ttu-id="79ce0-126">Escribir código de servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="79ce0-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

