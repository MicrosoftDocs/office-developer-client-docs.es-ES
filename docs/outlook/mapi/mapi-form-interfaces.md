---
title: Interfaces de formulario MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412348"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="f05c7-103">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="f05c7-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="f05c7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f05c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f05c7-105">MAPI define las interfaces siguientes relacionadas con los formularios.</span><span class="sxs-lookup"><span data-stu-id="f05c7-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="f05c7-106">**Nombre de la interfaz**</span><span class="sxs-lookup"><span data-stu-id="f05c7-106">**Interface name**</span></span>|<span data-ttu-id="f05c7-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f05c7-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f05c7-108">IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="f05c7-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="f05c7-109">Manipula objetos de formulario y controla comandos de objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="f05c7-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="f05c7-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f05c7-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="f05c7-111">Determina si el objeto de formulario puede controlar el siguiente mensaje y cambia el estado siguiente o anterior del objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="f05c7-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="f05c7-112">IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="f05c7-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="f05c7-113">Admite la instalación, la desinstalación y la resolución de servidores de formulario en un contenedor de formulario específico.</span><span class="sxs-lookup"><span data-stu-id="f05c7-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="f05c7-114">IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="f05c7-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="f05c7-115">Admite el uso de servidores de formulario en tiempo de ejecución configurables.</span><span class="sxs-lookup"><span data-stu-id="f05c7-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="f05c7-116">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="f05c7-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="f05c7-117">Permite a las aplicaciones cliente trabajar con propiedades específicas de una clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f05c7-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="f05c7-118">IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="f05c7-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="f05c7-119">Permite que las aplicaciones cliente obtengan información sobre los servidores de formulario, activen los servidores de formulario e instalen servidores de formulario en el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="f05c7-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="f05c7-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="f05c7-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="f05c7-121">Se usa para manipular mensajes asociados con objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="f05c7-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="f05c7-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f05c7-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="f05c7-123">Notifica a las aplicaciones cliente que se ha producido un evento en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="f05c7-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="f05c7-124">IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="f05c7-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="f05c7-125">Se usa para responder a los comandos Next, Previous y Delete del objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="f05c7-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="f05c7-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="f05c7-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="f05c7-127">Se usa para guardar, inicializar y cargar objetos de formulario desde y hacia el almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f05c7-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="f05c7-128">Para obtener más información acerca de los métodos de las interfaces de formulario MAPI, vea la documentación de estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="f05c7-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="f05c7-129">No es necesario implementar todas las interfaces de formulario MAPI para crear un formulario personalizado.</span><span class="sxs-lookup"><span data-stu-id="f05c7-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="f05c7-130">Un formulario en sí solo requiere que implemente las **interfaces IPersistMessage**, **IMAPIForm** e **IMAPIFormAdviseSink.**</span><span class="sxs-lookup"><span data-stu-id="f05c7-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="f05c7-131">Además, también es una buena idea implementar **IMAPIFormFactory** e **IMAPIFormInfo**.</span><span class="sxs-lookup"><span data-stu-id="f05c7-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="f05c7-132">**IMAPIFormFactory** es útil para el cumplimiento de OLE y **IMAPIFormInfo** permite que las aplicaciones cliente bien escritas hagan un mejor uso de los formularios.</span><span class="sxs-lookup"><span data-stu-id="f05c7-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f05c7-133">Estrictamente hablando, **IMAPIFormAdviseSink** es una interfaz opcional.</span><span class="sxs-lookup"><span data-stu-id="f05c7-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="f05c7-134">Sin embargo, se recomienda encarecidamente implementarlo en los servidores de formulario.</span><span class="sxs-lookup"><span data-stu-id="f05c7-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="f05c7-135">Esta interfaz es fundamental para una interacción eficaz entre clientes de mensajería y servidores de formulario, especialmente cuando se tratan varios mensajes de la clase de mensaje del servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="f05c7-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f05c7-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f05c7-136">See also</span></span>



[<span data-ttu-id="f05c7-137">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="f05c7-137">MAPI Forms</span></span>](mapi-forms.md)

