---
title: IUnknown IMAPIMessageSite
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
ms.openlocfilehash: bf21ed1d41a61f600cfded777b699cf620c2e00f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321353"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="d9a92-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9a92-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="d9a92-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9a92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9a92-105">Manipula mensajes y se implementa mediante el código del visor de formularios (normalmente una aplicación cliente) que responde a dicha manipulación.</span><span class="sxs-lookup"><span data-stu-id="d9a92-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9a92-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d9a92-106">Header file:</span></span>  <br/> |<span data-ttu-id="d9a92-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="d9a92-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="d9a92-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="d9a92-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="d9a92-109">Objetos de sitio de mensaje</span><span class="sxs-lookup"><span data-stu-id="d9a92-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="d9a92-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d9a92-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="d9a92-111">Visores de formularios</span><span class="sxs-lookup"><span data-stu-id="d9a92-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="d9a92-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d9a92-112">Called by:</span></span>  <br/> |<span data-ttu-id="d9a92-113">Objetos de formulario</span><span class="sxs-lookup"><span data-stu-id="d9a92-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="d9a92-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="d9a92-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d9a92-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="d9a92-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="d9a92-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="d9a92-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="d9a92-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="d9a92-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d9a92-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="d9a92-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d9a92-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="d9a92-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="d9a92-120">Devuelve la sesión MAPI en la que se ha abierto o creado el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="d9a92-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="d9a92-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="d9a92-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="d9a92-122">Devuelve el almacén de mensajes que contiene el mensaje actual, si existe dicho almacén.</span><span class="sxs-lookup"><span data-stu-id="d9a92-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="d9a92-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="d9a92-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="d9a92-124">Devuelve la carpeta en la que se ha creado o abierto el mensaje actual, si existe una carpeta de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="d9a92-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="d9a92-125">GetMessage</span><span class="sxs-lookup"><span data-stu-id="d9a92-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="d9a92-126">Devuelve el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="d9a92-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="d9a92-127">GetFormManager</span><span class="sxs-lookup"><span data-stu-id="d9a92-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="d9a92-128">Devuelve una interfaz del administrador de formularios que un servidor de formularios puede usar para abrir otro servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="d9a92-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="d9a92-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="d9a92-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="d9a92-130">Crea un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="d9a92-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="d9a92-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="d9a92-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="d9a92-132">Copia el mensaje actual en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d9a92-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="d9a92-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="d9a92-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="d9a92-134">Mueve el mensaje actual a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d9a92-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="d9a92-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="d9a92-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="d9a92-136">Elimina el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="d9a92-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="d9a92-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="d9a92-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="d9a92-138">Solicita que se guarde el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="d9a92-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="d9a92-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="d9a92-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="d9a92-140">Solicita que el mensaje actual se ponga en cola para su entrega.</span><span class="sxs-lookup"><span data-stu-id="d9a92-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="d9a92-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="d9a92-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="d9a92-142">Devuelve información de un objeto de sitio de mensaje sobre las funciones del sitio de mensaje para el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="d9a92-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="d9a92-143">Volvió</span><span class="sxs-lookup"><span data-stu-id="d9a92-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="d9a92-144">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produce en el objeto de sitio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d9a92-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9a92-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9a92-145">See also</span></span>



[<span data-ttu-id="d9a92-146">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="d9a92-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

