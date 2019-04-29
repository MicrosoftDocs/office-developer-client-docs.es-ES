---
title: Implementar un visor de formularios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435820"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="18316-103">Implementar un visor de formularios</span><span class="sxs-lookup"><span data-stu-id="18316-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="18316-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18316-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18316-105">Un visor de formularios incluye tres objetos: un sitio de mensajes, un receptor de notificaciones de vista y un contexto de vista.</span><span class="sxs-lookup"><span data-stu-id="18316-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="18316-106">Cada uno de estos objetos permite interactuar con un servidor de formularios y sus formularios.</span><span class="sxs-lookup"><span data-stu-id="18316-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="18316-107">Un sitio de mensaje es un objeto que implementa la interfaz [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) y ayuda a los servidores de formularios con tareas como mover, guardar o eliminar mensajes, crear nuevos mensajes o iniciar nuevos servidores de formularios.</span><span class="sxs-lookup"><span data-stu-id="18316-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="18316-108">Los formularios usan los sitios de mensajes para obtener información sobre el estado del cliente con respecto a varios proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="18316-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="18316-109">Por ejemplo, un formulario puede usar el sitio de mensajes para obtener un puntero a su almacén de mensajes actual, un mensaje o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="18316-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="18316-110">Hay dos tipos de métodos en la interfaz **IMAPIMessageSite** :</span><span class="sxs-lookup"><span data-stu-id="18316-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="18316-111">Métodos que proporcionan información a los objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="18316-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="18316-112">Métodos que manipulan mensajes.</span><span class="sxs-lookup"><span data-stu-id="18316-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="18316-113">Los métodos que proporcionan información a los objetos de formulario son sencillos de implementar.</span><span class="sxs-lookup"><span data-stu-id="18316-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="18316-114">En todos los casos excepto [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md), ya debe tener disponible la información que necesita cada método.</span><span class="sxs-lookup"><span data-stu-id="18316-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="18316-115">Los métodos que manipulan mensajes deben actuar como si se hubieran desencadenado a través de la interfaz de usuario normal.</span><span class="sxs-lookup"><span data-stu-id="18316-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="18316-116">Por ejemplo, si un objeto de formulario llama al método [IMAPIMessageSite:: NewMessage](imapimessagesite-newmessage.md) , se comportará como si el usuario hubiese elegido redactar un nuevo mensaje personalizado con la interfaz de usuario normal.</span><span class="sxs-lookup"><span data-stu-id="18316-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="18316-117">Los comandos que normalmente generan este comportamiento son **redactar**, **abrir**, **responder**, **responder a todos los destinatarios**y reenviar. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="18316-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="18316-118">Un contexto de vista es un objeto que implementa la interfaz [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) y proporciona a los servidores de formularios un contexto para el mensaje actual, lo que permite a los servidores cambiar fácilmente al mensaje siguiente o anterior de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="18316-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="18316-119">Un formulario usa un contexto de vista para compartir información.</span><span class="sxs-lookup"><span data-stu-id="18316-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="18316-120">Con un objeto de contexto de vista, un formulario puede:</span><span class="sxs-lookup"><span data-stu-id="18316-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="18316-121">Regístrese con su cliente para obtener notificaciones.</span><span class="sxs-lookup"><span data-stu-id="18316-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="18316-122">Activar el mensaje siguiente o anterior de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="18316-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="18316-123">Obtener información de impresión.</span><span class="sxs-lookup"><span data-stu-id="18316-123">Get printing information.</span></span>
    
- <span data-ttu-id="18316-124">Obtener el estado del cliente.</span><span class="sxs-lookup"><span data-stu-id="18316-124">Get your client's status.</span></span>
    
- <span data-ttu-id="18316-125">Obtener una secuencia que se puede usar para guardar la versión de texto de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="18316-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="18316-126">De forma similar a los métodos de la interfaz [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) , los métodos de **IMAPIViewContext** se relacionan con las acciones de usuario y las características de cliente que se relacionan con el contexto de la vista.</span><span class="sxs-lookup"><span data-stu-id="18316-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="18316-127">Por ejemplo, un contexto de vista está implicado en la activación del mensaje siguiente o anterior, la ordenación del contenido de la carpeta y el filtrado del contenido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="18316-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="18316-128">No es importante qué mecanismo se proporciona a los usuarios para activar estas características, sólo es importante que la semántica de dichas características se asigne correctamente a los métodos de la interfaz **IMAPIViewContext** .</span><span class="sxs-lookup"><span data-stu-id="18316-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="18316-129">Un receptor View Advise es un objeto que implementa la interfaz [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) y controla las notificaciones de los servidores de formularios que afectan al visor, y a los formularios y visores de formulario de ayuda para trabajar juntos.</span><span class="sxs-lookup"><span data-stu-id="18316-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="18316-130">Para obtener más información, consulte [enviar y recibir notificaCiones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="18316-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

