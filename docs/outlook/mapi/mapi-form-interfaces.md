---
title: Interfaces de formulario de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351544"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="d8d29-103">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="d8d29-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="d8d29-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8d29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8d29-105">MAPI define las siguientes interfaces relacionadas con los formularios.</span><span class="sxs-lookup"><span data-stu-id="d8d29-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="d8d29-106">**Nombre de interfaz**</span><span class="sxs-lookup"><span data-stu-id="d8d29-106">**Interface name**</span></span>|<span data-ttu-id="d8d29-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8d29-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8d29-108">IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="d8d29-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="d8d29-109">Manipula los objetos de formulario y controla los comandos de objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="d8d29-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="d8d29-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d8d29-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="d8d29-111">Determina si el objeto de formulario puede controlar el siguiente mensaje y cambia el estado siguiente o anterior del objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="d8d29-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="d8d29-112">IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="d8d29-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="d8d29-113">Admite la instalación, desinstalación y resolución de servidores de formularios en un contenedor de formularios específico.</span><span class="sxs-lookup"><span data-stu-id="d8d29-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="d8d29-114">IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="d8d29-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="d8d29-115">Admite el uso de servidores de formulario en tiempo de ejecución configurables.</span><span class="sxs-lookup"><span data-stu-id="d8d29-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="d8d29-116">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="d8d29-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="d8d29-117">Permite a las aplicaciones cliente trabajar con propiedades específicas de una clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d8d29-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="d8d29-118">IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="d8d29-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="d8d29-119">Permite a las aplicaciones cliente obtener información acerca de los servidores de formularios, activar servidores de formularios e instalar servidores de formularios en el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="d8d29-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="d8d29-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="d8d29-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="d8d29-121">Se usa para manipular los mensajes asociados con objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="d8d29-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="d8d29-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d8d29-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="d8d29-123">Notifica a las aplicaciones cliente que se ha producido un evento en el objeto Form.</span><span class="sxs-lookup"><span data-stu-id="d8d29-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="d8d29-124">IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="d8d29-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="d8d29-125">Se usa para responder a los comandos siguiente, anterior y eliminar en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="d8d29-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="d8d29-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="d8d29-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="d8d29-127">Se usa para guardar, inicializar y cargar objetos de formulario en el almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d8d29-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="d8d29-128">Para obtener más información acerca de los métodos de las interfaces de formulario de MAPI, vea la documentación de estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="d8d29-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="d8d29-129">No es necesario implementar todas las interfaces de formulario MAPI para crear un formulario personalizado.</span><span class="sxs-lookup"><span data-stu-id="d8d29-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="d8d29-130">Un formulario solo requiere que se implementen las interfaces **IPersistMessage**, **IMAPIForm**y **IMAPIFormAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="d8d29-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="d8d29-131">Además, también es una buena idea implementar **IMAPIFormFactory** y **IMAPIFormInfo**.</span><span class="sxs-lookup"><span data-stu-id="d8d29-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="d8d29-132">**IMAPIFormFactory** es útil para el cumplimiento de OLE, y **IMAPIFormInfo** permite que las aplicaciones de cliente bien escritas usen mejor los formularios.</span><span class="sxs-lookup"><span data-stu-id="d8d29-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d8d29-133">Hablando estrictamente, **IMAPIFormAdviseSink** es una interfaz opcional.</span><span class="sxs-lookup"><span data-stu-id="d8d29-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="d8d29-134">Sin embargo, se recomienda encarecidamente implementarlo en los servidores de formularios.</span><span class="sxs-lookup"><span data-stu-id="d8d29-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="d8d29-135">Esta interfaz es fundamental para la interacción eficaz entre los clientes de mensajería y los servidores de formularios, sobre todo cuando se trata de varios mensajes de la clase de mensaje de su servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="d8d29-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8d29-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8d29-136">See also</span></span>



[<span data-ttu-id="d8d29-137">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="d8d29-137">MAPI Forms</span></span>](mapi-forms.md)

