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
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309607"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="b89ee-103">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b89ee-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="b89ee-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b89ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b89ee-105">Permite a los visores de formulario controlar el almacenamiento de un formulario y realizar la transición entre los distintos estados.</span><span class="sxs-lookup"><span data-stu-id="b89ee-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b89ee-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b89ee-106">Header file:</span></span>  <br/> |<span data-ttu-id="b89ee-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="b89ee-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="b89ee-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="b89ee-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b89ee-109">Conservar objetos de mensaje</span><span class="sxs-lookup"><span data-stu-id="b89ee-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="b89ee-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b89ee-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b89ee-111">Objetos de formulario</span><span class="sxs-lookup"><span data-stu-id="b89ee-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="b89ee-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b89ee-112">Called by:</span></span>  <br/> |<span data-ttu-id="b89ee-113">Visores de formularios</span><span class="sxs-lookup"><span data-stu-id="b89ee-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="b89ee-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="b89ee-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b89ee-115">IID_IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="b89ee-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="b89ee-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="b89ee-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b89ee-117">LPPERSISTMESSAGE</span><span class="sxs-lookup"><span data-stu-id="b89ee-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b89ee-118">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="b89ee-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b89ee-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="b89ee-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="b89ee-120">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="b89ee-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="b89ee-121">GetClassID</span><span class="sxs-lookup"><span data-stu-id="b89ee-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="b89ee-122">Devuelve un identificador que representa el servidor de formularios que puede administrar el formulario.</span><span class="sxs-lookup"><span data-stu-id="b89ee-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="b89ee-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="b89ee-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="b89ee-124">Comprueba en el formulario los cambios realizados desde la última vez que se guardaron.</span><span class="sxs-lookup"><span data-stu-id="b89ee-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="b89ee-125">InitNew</span><span class="sxs-lookup"><span data-stu-id="b89ee-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="b89ee-126">Inicializa un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="b89ee-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="b89ee-127">Load</span><span class="sxs-lookup"><span data-stu-id="b89ee-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="b89ee-128">Carga el formulario para un mensaje especificado.</span><span class="sxs-lookup"><span data-stu-id="b89ee-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="b89ee-129">Save</span><span class="sxs-lookup"><span data-stu-id="b89ee-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="b89ee-130">Guarda un formulario revisado en el mensaje desde el que se cargó o creó.</span><span class="sxs-lookup"><span data-stu-id="b89ee-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="b89ee-131">SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="b89ee-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="b89ee-132">Notifica al formulario que se ha completado una operación de guardado.</span><span class="sxs-lookup"><span data-stu-id="b89ee-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="b89ee-133">HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="b89ee-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="b89ee-134">Hace que el formulario libere su mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="b89ee-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b89ee-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b89ee-135">Remarks</span></span>

<span data-ttu-id="b89ee-136">Todos los formularios son necesarios para implementar la **interfaz IPersistMessage.**</span><span class="sxs-lookup"><span data-stu-id="b89ee-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="b89ee-137">**IPersistMessage funciona** de forma similar a la interfaz OLE [IPersistStorage.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b89ee-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="b89ee-138">Para obtener más información, vea los **métodos IPersistStorage.**</span><span class="sxs-lookup"><span data-stu-id="b89ee-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b89ee-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b89ee-139">See also</span></span>



[<span data-ttu-id="b89ee-140">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b89ee-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

