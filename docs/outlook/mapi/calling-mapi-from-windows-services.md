---
title: Llamar a MAPI desde Windows Services
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318111"
---
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="1a83f-103">Llamar a MAPI desde Windows Services</span><span class="sxs-lookup"><span data-stu-id="1a83f-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="1a83f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a83f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a83f-105">Para permitir que las aplicaciones cliente MAPI que se escriben como servicios Windows funcionen con proveedores de servicios compatibles con MAPI, MAPI impone varias limitaciones y requisitos.</span><span class="sxs-lookup"><span data-stu-id="1a83f-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="1a83f-106">Los clientes MAPI tienen las siguientes limitaciones:</span><span class="sxs-lookup"><span data-stu-id="1a83f-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="1a83f-107">No pueden permitir una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1a83f-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="1a83f-108">Solo pueden enviar mensajes a través de un proveedor de transporte y un almacén de mensajes estrechamente acoplados.</span><span class="sxs-lookup"><span data-stu-id="1a83f-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="1a83f-109">Además, los clientes MAPI pueden enviar y recibir mensajes mediante el Microsoft Exchange Server u otro proveedor de transporte basado en servidor.</span><span class="sxs-lookup"><span data-stu-id="1a83f-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="1a83f-110">Debido a problemas de identidad y seguridad entre las aplicaciones cliente y la cola MAPI, la mayoría de los proveedores de transporte no se admiten en un servicio.</span><span class="sxs-lookup"><span data-stu-id="1a83f-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="1a83f-111">Todas las aplicaciones cliente MAPI, tanto si se implementan como servicios Windows, deben llamar a la [función MAPIInitialize](mapiinitialize.md) para inicializar las bibliotecas MAPI.</span><span class="sxs-lookup"><span data-stu-id="1a83f-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="1a83f-112">También es necesaria una llamada [a la función OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) para usar las bibliotecas OLE.</span><span class="sxs-lookup"><span data-stu-id="1a83f-112">A call to the [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="1a83f-113">Tanto [MAPIInitialize](mapiinitialize.md) como [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) hacen llamadas a la función [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) para inicializar las bibliotecas del Modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="1a83f-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="1a83f-114">Los clientes que son servicios deben establecer una marca especial, MAPI_NT_SERVICE, en el **miembro ulFlags** de la estructura [de MAPIINIT_0](mapiinit_0.md) que se pasa a [MAPIInitialize](mapiinitialize.md) y en el parámetro  _ulFlags_ que se pasa a la función [MAPILogonEx](mapilogonex.md) para informar a MAPI de su implementación especial.</span><span class="sxs-lookup"><span data-stu-id="1a83f-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="1a83f-115">Los clientes MAPI escritos como Windows y escritos con la interfaz de cliente MAPI tienen un requisito adicional.</span><span class="sxs-lookup"><span data-stu-id="1a83f-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="1a83f-116">Deben establecer la marca MAPI_NO_MAIL en la llamada en [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="1a83f-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="1a83f-117">Otros tipos de clientes no tienen que establecer una marca para el inicio de sesión porque MAPI la establece automáticamente.</span><span class="sxs-lookup"><span data-stu-id="1a83f-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="1a83f-118">Para controlar los mensajes en un subproceso de inicialización, un cliente MAPI que se implementa como servicio hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1a83f-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="1a83f-119">Llama a [la función MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) cuando el subproceso principal se bloquea.</span><span class="sxs-lookup"><span data-stu-id="1a83f-119">Calls the [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="1a83f-120">Llama a la secuencia [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)y [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) de las funciones Windows para controlar el mensaje cuando [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) devuelve la suma del valor del parámetro _nCount_ y el valor de **WAIT_OBJECT_0**, lo que indica que un mensaje está en la cola.</span><span class="sxs-lookup"><span data-stu-id="1a83f-120">Calls the [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a83f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a83f-121">See also</span></span>



[<span data-ttu-id="1a83f-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="1a83f-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="1a83f-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="1a83f-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="1a83f-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="1a83f-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="1a83f-125">Problemas del entorno operativo</span><span class="sxs-lookup"><span data-stu-id="1a83f-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

