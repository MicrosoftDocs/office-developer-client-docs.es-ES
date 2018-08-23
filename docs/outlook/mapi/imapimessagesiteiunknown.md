---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cffa3024b8533f07f8f76fa5bbac219e23d61bdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589507"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="a0588-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0588-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="a0588-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0588-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0588-105">Manipula los mensajes y se implementa mediante el código de formulario Visor (normalmente, una aplicación de cliente) que responde a esa manipulación.</span><span class="sxs-lookup"><span data-stu-id="a0588-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0588-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a0588-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0588-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="a0588-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a0588-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="a0588-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a0588-109">Objetos de sitio de mensaje</span><span class="sxs-lookup"><span data-stu-id="a0588-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="a0588-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="a0588-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a0588-111">Visores de formulario</span><span class="sxs-lookup"><span data-stu-id="a0588-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="a0588-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a0588-112">Called by:</span></span>  <br/> |<span data-ttu-id="a0588-113">Objetos de formulario</span><span class="sxs-lookup"><span data-stu-id="a0588-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="a0588-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="a0588-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a0588-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="a0588-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="a0588-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="a0588-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a0588-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="a0588-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a0588-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="a0588-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a0588-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="a0588-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="a0588-120">Devuelve la sesión MAPI en el que se ha creado o abierto el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="a0588-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="a0588-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="a0588-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="a0588-122">Devuelve el almacén de mensajes que contiene el mensaje actual, si existe un almacén de este tipo.</span><span class="sxs-lookup"><span data-stu-id="a0588-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="a0588-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="a0588-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="a0588-124">Devuelve la carpeta en la que el mensaje actual se ha creado o abierto, si existe una carpeta de este tipo.</span><span class="sxs-lookup"><span data-stu-id="a0588-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="a0588-125">GetMessage</span><span class="sxs-lookup"><span data-stu-id="a0588-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="a0588-126">Devuelve el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="a0588-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="a0588-127">GetFormManager</span><span class="sxs-lookup"><span data-stu-id="a0588-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="a0588-128">Devuelve una interfaz de administrador de formulario, que puede usar un servidor de formulario para abrir otro servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="a0588-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="a0588-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="a0588-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="a0588-130">Crea un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="a0588-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="a0588-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="a0588-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="a0588-132">Copia el mensaje actual en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a0588-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="a0588-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="a0588-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="a0588-134">Mueve el mensaje actual a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a0588-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="a0588-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="a0588-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="a0588-136">Elimina el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="a0588-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="a0588-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="a0588-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="a0588-138">Solicitudes que se guarde el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="a0588-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="a0588-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="a0588-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="a0588-140">Solicitudes que se ponen en cola en el mensaje actual para la entrega.</span><span class="sxs-lookup"><span data-stu-id="a0588-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="a0588-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="a0588-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="a0588-142">Devuelve información de un objeto de sitio de mensaje acerca del mensaje de las capacidades del sitio para el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="a0588-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="a0588-143">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a0588-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="a0588-144">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el que se producen en el objeto de sitio de mensaje de error anterior.</span><span class="sxs-lookup"><span data-stu-id="a0588-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0588-145">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a0588-145">See also</span></span>



[<span data-ttu-id="a0588-146">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a0588-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

