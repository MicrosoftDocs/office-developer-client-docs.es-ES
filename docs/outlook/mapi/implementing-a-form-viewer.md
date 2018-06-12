---
title: Implementación de un visor de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 645f98342b4b3ec2bebf3f233f719bd5cae69da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817659"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="c0547-103">Implementación de un visor de formulario</span><span class="sxs-lookup"><span data-stu-id="c0547-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="c0547-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0547-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0547-105">Un visor de formulario incluye tres objetos: un sitio de mensaje, una vista de aviso receptor y un contexto de vista.</span><span class="sxs-lookup"><span data-stu-id="c0547-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="c0547-106">Cada uno de estos objetos permite interactuar con un servidor de formulario y sus formularios.</span><span class="sxs-lookup"><span data-stu-id="c0547-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="c0547-107">Un sitio de mensaje es un objeto que implementa el [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) de la interfaz y ayuda a los servidores de formulario con las tareas, como mover, guardar o eliminar mensajes, creación de nuevos mensajes o iniciar nuevos servidores de formulario.</span><span class="sxs-lookup"><span data-stu-id="c0547-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="c0547-108">Sitios de mensaje se usan los formularios para obtener información acerca del estado de su cliente con respecto a varios proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="c0547-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="c0547-109">Por ejemplo, un formulario puede usar el sitio de mensaje para obtener un puntero a su almacén de mensajes actual, un mensaje o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c0547-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="c0547-110">Hay dos tipos de métodos en la interfaz de **IMAPIMessageSite** :</span><span class="sxs-lookup"><span data-stu-id="c0547-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="c0547-111">Métodos que proporcionan información a los objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="c0547-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="c0547-112">Métodos que manipulan los mensajes.</span><span class="sxs-lookup"><span data-stu-id="c0547-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="c0547-113">Los métodos que proporcionan información a los objetos de formulario son sencillos de implementar.</span><span class="sxs-lookup"><span data-stu-id="c0547-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="c0547-114">En todos los casos excepto [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), debe tener disponible la información necesaria en cada método.</span><span class="sxs-lookup"><span data-stu-id="c0547-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="c0547-115">Los métodos que manipulan mensajes deben actuar como si hubiera desencadenado a través de la interfaz de usuario normal.</span><span class="sxs-lookup"><span data-stu-id="c0547-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="c0547-116">Por ejemplo, si un objeto de formulario llama al método [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) , se comportan como si el usuario ha elegido redactar un nuevo mensaje personalizado con la interfaz de usuario normal.</span><span class="sxs-lookup"><span data-stu-id="c0547-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="c0547-117">Los comandos que suelen generan este comportamiento son **redacción**, **Abrir**, **responder**, **responder a todos los destinatarios**y **hacia delante**.</span><span class="sxs-lookup"><span data-stu-id="c0547-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="c0547-118">Un contexto de vista es un objeto que implementa el [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) de la interfaz y proporciona servidores de formulario con un contexto para el mensaje actual, lo que permite a los servidores cambiar fácilmente al mensaje siguiente o anterior en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="c0547-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="c0547-119">Un formulario, utiliza un contexto de vista para compartir información.</span><span class="sxs-lookup"><span data-stu-id="c0547-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="c0547-120">Con un objeto de contexto de vista, un formulario puede:</span><span class="sxs-lookup"><span data-stu-id="c0547-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="c0547-121">Registrar con su cliente para las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="c0547-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="c0547-122">Activar el mensaje siguiente o anterior en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="c0547-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="c0547-123">Obtenga información de impresión.</span><span class="sxs-lookup"><span data-stu-id="c0547-123">Get printing information.</span></span>
    
- <span data-ttu-id="c0547-124">Obtener el estado de su cliente.</span><span class="sxs-lookup"><span data-stu-id="c0547-124">Get your client's status.</span></span>
    
- <span data-ttu-id="c0547-125">Obtener una secuencia que se puede usar para guardar la versión de texto de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c0547-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="c0547-126">Similar a los métodos en el [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) interfaz, los métodos en **IMAPIViewContext** correlacionan con las acciones del usuario y las características de cliente que se relacionan con el contexto de vista.</span><span class="sxs-lookup"><span data-stu-id="c0547-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="c0547-127">Por ejemplo, un contexto de vista consiste en activar el mensaje siguiente o anterior, ordenar el contenido de la carpeta y filtrar el contenido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="c0547-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="c0547-128">No es importante qué mecanismo de proporcionar a los usuarios para activar estas características, solo es importante que la semántica de esas características se asigna a los métodos en la interfaz de **IMAPIViewContext** .</span><span class="sxs-lookup"><span data-stu-id="c0547-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="c0547-129">Una vista de aviso receptor es un objeto que implementa el [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) interfaz y controladores de notificaciones desde servidores de formulario que afectan a la Ayuda y el Visor de formularios y los visores de formulario para que trabajen conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="c0547-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="c0547-130">Para obtener más información, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="c0547-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

