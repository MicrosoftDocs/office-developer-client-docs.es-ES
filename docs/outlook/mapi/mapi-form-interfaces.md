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
ms.openlocfilehash: 8452a6e49059dd0912f1efffef7e749afd6cdf6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818112"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="9f10c-103">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="9f10c-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="9f10c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f10c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f10c-105">MAPI define las interfaces siguientes relativas a los formularios.</span><span class="sxs-lookup"><span data-stu-id="9f10c-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="9f10c-106">**Nombre de la interfaz**</span><span class="sxs-lookup"><span data-stu-id="9f10c-106">**Interface name**</span></span>|<span data-ttu-id="9f10c-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9f10c-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9f10c-108">IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="9f10c-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="9f10c-109">Manipula los objetos formulario y administra los comandos de objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="9f10c-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="9f10c-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="9f10c-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="9f10c-111">Determina si el objeto de formulario, puede controlar el siguiente mensaje y cambia el estado siguiente o anterior del objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="9f10c-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="9f10c-112">IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="9f10c-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="9f10c-113">Es compatible con la instalación, desinstalación y solución de servidores de formulario frente a un contenedor de forma específicos.</span><span class="sxs-lookup"><span data-stu-id="9f10c-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="9f10c-114">IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="9f10c-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="9f10c-115">Admite el uso de servidores de formulario configurable de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="9f10c-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="9f10c-116">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="9f10c-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="9f10c-117">Permite a las aplicaciones de cliente trabajar con las propiedades que son específicas de una clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f10c-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="9f10c-118">IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="9f10c-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="9f10c-119">Permite a las aplicaciones de cliente obtener información acerca de los servidores de formulario, activa los servidores de formulario y servidores de formulario se instala en el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="9f10c-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="9f10c-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="9f10c-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="9f10c-121">Se usa para manipular los mensajes asociados a objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="9f10c-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="9f10c-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="9f10c-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="9f10c-123">Notifica a las aplicaciones de cliente que se ha producido un evento en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="9f10c-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="9f10c-124">IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="9f10c-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="9f10c-125">Se usa para responder a la siguiente, anterior y eliminar comandos en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="9f10c-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="9f10c-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="9f10c-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="9f10c-127">Se usa para guardar, inicializar y cargar los objetos de formulario a y desde el almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9f10c-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="9f10c-128">Para obtener más información acerca de los métodos de las interfaces de formulario MAPI, consulte la documentación para estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="9f10c-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="9f10c-129">No es necesario implementar todas las interfaces de formulario MAPI para crear un formulario personalizado.</span><span class="sxs-lookup"><span data-stu-id="9f10c-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="9f10c-130">Un formulario propio sólo requiere que implementar el **IPersistMessage**, **IMAPIForm**, y **IMAPIFormAdviseSink** interfaces.</span><span class="sxs-lookup"><span data-stu-id="9f10c-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="9f10c-131">Además, también es una buena idea para implementar **IMAPIFormFactory** y **IMAPIFormInfo**.</span><span class="sxs-lookup"><span data-stu-id="9f10c-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="9f10c-132">**IMAPIFormFactory** es útil para el cumplimiento de OLE y **IMAPIFormInfo** permite a las aplicaciones cliente bien escrito hacer un mejor uso de los formularios.</span><span class="sxs-lookup"><span data-stu-id="9f10c-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9f10c-133">En realidad, **IMAPIFormAdviseSink** es una interfaz opcional.</span><span class="sxs-lookup"><span data-stu-id="9f10c-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="9f10c-134">Sin embargo, se recomienda encarecidamente que se implemente en los servidores de formulario.</span><span class="sxs-lookup"><span data-stu-id="9f10c-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="9f10c-135">Esta interfaz es fundamental para la interacción eficaz entre clientes de mensajería y los servidores de formulario, especialmente cuando varios mensajes de su servidor de formulario clase de mensaje que se trate.</span><span class="sxs-lookup"><span data-stu-id="9f10c-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f10c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f10c-136">See also</span></span>



[<span data-ttu-id="9f10c-137">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="9f10c-137">MAPI Forms</span></span>](mapi-forms.md)

