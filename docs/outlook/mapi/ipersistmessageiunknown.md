---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 62fb2b069a50408713eea741cf837c421a749fcd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817895"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="b72c6-103">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b72c6-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="b72c6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b72c6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b72c6-105">Permite que los visores de formulario controlar el almacenamiento de un formulario y para la transición entre los distintos Estados.</span><span class="sxs-lookup"><span data-stu-id="b72c6-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b72c6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b72c6-106">Header file:</span></span>  <br/> |<span data-ttu-id="b72c6-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="b72c6-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="b72c6-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="b72c6-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b72c6-109">Conservar los objetos de mensaje</span><span class="sxs-lookup"><span data-stu-id="b72c6-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="b72c6-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="b72c6-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b72c6-111">Objetos de formulario</span><span class="sxs-lookup"><span data-stu-id="b72c6-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="b72c6-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b72c6-112">Called by:</span></span>  <br/> |<span data-ttu-id="b72c6-113">Visores de formulario</span><span class="sxs-lookup"><span data-stu-id="b72c6-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="b72c6-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="b72c6-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b72c6-115">IID_IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="b72c6-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="b72c6-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="b72c6-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b72c6-117">LPPERSISTMESSAGE</span><span class="sxs-lookup"><span data-stu-id="b72c6-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b72c6-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="b72c6-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b72c6-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="b72c6-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="b72c6-120">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="b72c6-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="b72c6-121">GetClassID</span><span class="sxs-lookup"><span data-stu-id="b72c6-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="b72c6-122">Devuelve un identificador que representa el servidor de formulario que puede administrar el formulario.</span><span class="sxs-lookup"><span data-stu-id="b72c6-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="b72c6-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="b72c6-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="b72c6-124">Comprueba el formulario para que los cambios realizados desde la última vez que guardó.</span><span class="sxs-lookup"><span data-stu-id="b72c6-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="b72c6-125">InitNew</span><span class="sxs-lookup"><span data-stu-id="b72c6-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="b72c6-126">Inicializa un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="b72c6-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="b72c6-127">Load</span><span class="sxs-lookup"><span data-stu-id="b72c6-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="b72c6-128">Carga el formulario para un mensaje especificado.</span><span class="sxs-lookup"><span data-stu-id="b72c6-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="b72c6-129">Save</span><span class="sxs-lookup"><span data-stu-id="b72c6-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="b72c6-130">Guarda un formulario revisado el mensaje desde la que se ha cargado o creado.</span><span class="sxs-lookup"><span data-stu-id="b72c6-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="b72c6-131">SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="b72c6-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="b72c6-132">Se notifica el formulario que guarda una operación se ha completado.</span><span class="sxs-lookup"><span data-stu-id="b72c6-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="b72c6-133">HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="b72c6-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="b72c6-134">Hace que el formulario liberar su mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="b72c6-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b72c6-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b72c6-135">Remarks</span></span>

<span data-ttu-id="b72c6-136">Todos los formularios necesarios para implementar la interfaz **IPersistMessage** .</span><span class="sxs-lookup"><span data-stu-id="b72c6-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="b72c6-137">**IPersistMessage** funciona de manera similar a la interfaz OLE [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b72c6-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="b72c6-138">Para obtener más información, vea los métodos **IPersistStorage** .</span><span class="sxs-lookup"><span data-stu-id="b72c6-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b72c6-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b72c6-139">See also</span></span>



[<span data-ttu-id="b72c6-140">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b72c6-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

