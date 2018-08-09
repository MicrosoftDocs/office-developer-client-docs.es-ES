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
ms.openlocfilehash: bce70d891bc33dcddb94fc05992c09991c6cdc63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817572"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="5d248-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5d248-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="5d248-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d248-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d248-105">Pase el proveedor de almacenamiento como un campo de la estructura MAPISIB durante una llamada a [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="5d248-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="5d248-106">El proveedor de almacenamiento usa esta interfaz para proporcionar comentarios a Microsoft Outlook sobre el estado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="5d248-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d248-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5d248-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="5d248-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="5d248-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="5d248-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="5d248-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="5d248-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="5d248-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="5d248-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="5d248-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="5d248-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5d248-112">Called by:</span></span>  <br/> |<span data-ttu-id="5d248-113">Proveedores de almacén</span><span class="sxs-lookup"><span data-stu-id="5d248-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="5d248-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="5d248-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5d248-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="5d248-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5d248-116">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="5d248-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5d248-117">Progress</span><span class="sxs-lookup"><span data-stu-id="5d248-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="5d248-118">El proveedor de almacenamiento periódicamente llama a esta función para actualizar el estado en el cuadro de diálogo de envío o recepción.</span><span class="sxs-lookup"><span data-stu-id="5d248-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="5d248-119">Error</span><span class="sxs-lookup"><span data-stu-id="5d248-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="5d248-120">Si se producen errores durante la sincronización, el proveedor de almacenamiento llama a esta función para proporcionar detalles que se muestran en el cuadro de diálogo de envío o recepción.</span><span class="sxs-lookup"><span data-stu-id="5d248-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="5d248-121">Hecho</span><span class="sxs-lookup"><span data-stu-id="5d248-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="5d248-122">El proveedor de almacenamiento llama a esta función para notificar a Outlook que se ha completado la sincronización.</span><span class="sxs-lookup"><span data-stu-id="5d248-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d248-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d248-123">See also</span></span>



[<span data-ttu-id="5d248-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5d248-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="5d248-125">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="5d248-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

