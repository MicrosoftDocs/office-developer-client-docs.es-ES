---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 33d811af0fc9e06902750075ba39bfb6ca88903f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593714"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="9de69-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9de69-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="9de69-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9de69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9de69-105">Pase el proveedor de almacenamiento como un campo de la estructura MAPISIB durante una llamada a [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="9de69-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="9de69-106">El proveedor de almacenamiento usa esta interfaz para proporcionar comentarios a Microsoft Outlook sobre el estado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="9de69-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9de69-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9de69-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="9de69-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="9de69-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="9de69-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="9de69-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="9de69-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="9de69-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9de69-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="9de69-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="9de69-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9de69-112">Called by:</span></span>  <br/> |<span data-ttu-id="9de69-113">Proveedores de almacén</span><span class="sxs-lookup"><span data-stu-id="9de69-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="9de69-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="9de69-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9de69-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="9de69-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9de69-116">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="9de69-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9de69-117">Progress</span><span class="sxs-lookup"><span data-stu-id="9de69-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="9de69-118">El proveedor de almacenamiento periódicamente llama a esta función para actualizar el estado en el cuadro de diálogo de envío o recepción.</span><span class="sxs-lookup"><span data-stu-id="9de69-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="9de69-119">Error</span><span class="sxs-lookup"><span data-stu-id="9de69-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="9de69-120">Si se producen errores durante la sincronización, el proveedor de almacenamiento llama a esta función para proporcionar detalles que se muestran en el cuadro de diálogo de envío o recepción.</span><span class="sxs-lookup"><span data-stu-id="9de69-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="9de69-121">Hecho</span><span class="sxs-lookup"><span data-stu-id="9de69-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="9de69-122">El proveedor de almacenamiento llama a esta función para notificar a Outlook que se ha completado la sincronización.</span><span class="sxs-lookup"><span data-stu-id="9de69-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9de69-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9de69-123">See also</span></span>



[<span data-ttu-id="9de69-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9de69-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="9de69-125">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="9de69-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

