---
title: IUnknown IMAPISyncProgressCallback
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
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341240"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="e7cc2-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7cc2-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="e7cc2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7cc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7cc2-105">Pasa el proveedor de almacenamiento como un campo de la estructura MAPISIB durante una llamada a [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="e7cc2-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="e7cc2-106">El proveedor de almacenamiento usa esta interfaz para proporcionar comentarios a Microsoft Outlook sobre el estado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="e7cc2-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7cc2-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e7cc2-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="e7cc2-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="e7cc2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e7cc2-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="e7cc2-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="e7cc2-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e7cc2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7cc2-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="e7cc2-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="e7cc2-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e7cc2-112">Called by:</span></span>  <br/> |<span data-ttu-id="e7cc2-113">Proveedores de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="e7cc2-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="e7cc2-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="e7cc2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e7cc2-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="e7cc2-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e7cc2-116">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="e7cc2-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e7cc2-117">Progress</span><span class="sxs-lookup"><span data-stu-id="e7cc2-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="e7cc2-118">El proveedor de almacén llama periódicamente a esta función para actualizar el estado en el cuadro de diálogo de envío y recepción.</span><span class="sxs-lookup"><span data-stu-id="e7cc2-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="e7cc2-119">Error</span><span class="sxs-lookup"><span data-stu-id="e7cc2-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="e7cc2-120">Si se detectan errores durante la sincronización, el proveedor del almacén llama a esta función para proporcionar detalles que se muestran en el cuadro de diálogo de envío o recepción.</span><span class="sxs-lookup"><span data-stu-id="e7cc2-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="e7cc2-121">Hecho</span><span class="sxs-lookup"><span data-stu-id="e7cc2-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="e7cc2-122">El proveedor del almacén llama a esta función para informar a Outlook de que la sincronización se ha completado.</span><span class="sxs-lookup"><span data-stu-id="e7cc2-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7cc2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7cc2-123">See also</span></span>



[<span data-ttu-id="e7cc2-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7cc2-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="e7cc2-125">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e7cc2-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

