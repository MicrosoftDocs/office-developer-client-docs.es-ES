---
title: Llamar a MAPI desde servicios de Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6465b2d24c3a38da40f2d1e6df79c2fa256b64b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816496"
---
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="985a6-103">Llamar a MAPI desde servicios de Windows</span><span class="sxs-lookup"><span data-stu-id="985a6-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="985a6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="985a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="985a6-105">Para habilitar las aplicaciones de cliente MAPI que se escriben como servicios de Windows para que funcione con los proveedores de servicio compatible con MAPI, MAPI impone varias limitaciones y requisitos.</span><span class="sxs-lookup"><span data-stu-id="985a6-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="985a6-106">Los clientes MAPI tienen las siguientes limitaciones:</span><span class="sxs-lookup"><span data-stu-id="985a6-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="985a6-107">No se permiten una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="985a6-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="985a6-108">Pueden enviar mensajes a través de un almacén de mensajes acoplado y transporte de proveedor.</span><span class="sxs-lookup"><span data-stu-id="985a6-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="985a6-109">Además, los clientes MAPI pueden enviar y recibir mensajes utilizando sólo el servidor de Exchange de Microsoft u otro proveedor de transporte basadas en servidor.</span><span class="sxs-lookup"><span data-stu-id="985a6-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="985a6-110">Debido a problemas de identidad y la seguridad entre las aplicaciones de cliente y la cola MAPI, la mayoría de los proveedores de transporte no se admite en un servicio.</span><span class="sxs-lookup"><span data-stu-id="985a6-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="985a6-111">Todas las aplicaciones de cliente MAPI, si se implementan como servicios de Windows, deben llamar a la función [MAPIInitialize](mapiinitialize.md) para inicializar las bibliotecas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="985a6-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="985a6-112">Una llamada a la función [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) también es necesaria usar las bibliotecas de OLE.</span><span class="sxs-lookup"><span data-stu-id="985a6-112">A call to the [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="985a6-113">[MAPIInitialize](mapiinitialize.md) y [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) realizan llamadas a la función [CoInitialize](http://msdn.microsoft.com/en-us/library/ms678543%28VS.85%29.aspx) para inicializar las bibliotecas de modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="985a6-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](http://msdn.microsoft.com/en-us/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="985a6-114">Los clientes que son servicios deben establecer un indicador especial, MAPI_NT_SERVICE, en el miembro **ulFlags** de la estructura [MAPIINIT_0](mapiinit_0.md) que se pasa a [MAPIInitialize](mapiinitialize.md) y en el parámetro _ulFlags_ que se pasa a la [MAPILogonEx](mapilogonex.md) función para informar a MAPI de su implementación especial.</span><span class="sxs-lookup"><span data-stu-id="985a6-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="985a6-115">Los clientes MAPI que se escriben como servicios de Windows y se escribe con la interfaz de cliente MAPI tienen un requisito adicional.</span><span class="sxs-lookup"><span data-stu-id="985a6-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="985a6-116">Debe establecer la marca MAPI_NO_MAIL en la llamada a [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="985a6-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="985a6-117">Otros tipos de clientes no es necesario que establecer una marca de inicio de sesión debido a que se establece automáticamente por MAPI.</span><span class="sxs-lookup"><span data-stu-id="985a6-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="985a6-118">Para administrar los mensajes en un subproceso de inicialización, un cliente MAPI que se implementa como un servicio hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="985a6-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="985a6-119">Llama a la función [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) cuando el subproceso principal se bloquea.</span><span class="sxs-lookup"><span data-stu-id="985a6-119">Calls the [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="985a6-120">Llama a la secuencia [GetMessage](http://msdn.microsoft.com/en-us/library/ms644936%28VS.85%29.aspx), [TranslateMessage](http://msdn.microsoft.com/en-us/library/ms644955%28VS.85%29.aspx)y [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934%28VS.85%29.aspx) de funciones de Windows para administrar el mensaje cuando [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) devuelve la suma del valor del parámetro _nCount_ y el valor de **WAIT_OBJECT_0**, que indica que es un mensaje en la cola.</span><span class="sxs-lookup"><span data-stu-id="985a6-120">Calls the [GetMessage](http://msdn.microsoft.com/en-us/library/ms644936%28VS.85%29.aspx), [TranslateMessage](http://msdn.microsoft.com/en-us/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="985a6-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="985a6-121">See also</span></span>



[<span data-ttu-id="985a6-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="985a6-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="985a6-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="985a6-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="985a6-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="985a6-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="985a6-125">Problemas del entorno operativo</span><span class="sxs-lookup"><span data-stu-id="985a6-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

