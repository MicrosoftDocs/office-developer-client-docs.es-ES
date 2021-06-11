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
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418340"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="46c27-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="46c27-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="46c27-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46c27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46c27-105">Pasa el proveedor de almacén como un campo en la estructura MAPISIB durante una llamada a [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="46c27-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="46c27-106">El proveedor de la tienda usa esta interfaz para proporcionar comentarios a Microsoft Outlook sobre el estado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="46c27-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46c27-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="46c27-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="46c27-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="46c27-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="46c27-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="46c27-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="46c27-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="46c27-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="46c27-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="46c27-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="46c27-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="46c27-112">Called by:</span></span>  <br/> |<span data-ttu-id="46c27-113">Proveedores de la tienda</span><span class="sxs-lookup"><span data-stu-id="46c27-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="46c27-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="46c27-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="46c27-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="46c27-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="46c27-116">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="46c27-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="46c27-117">Progress</span><span class="sxs-lookup"><span data-stu-id="46c27-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="46c27-118">El proveedor de almacenamiento llama periódicamente a esta función para actualizar el estado en el cuadro de diálogo Enviar y recibir.</span><span class="sxs-lookup"><span data-stu-id="46c27-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="46c27-119">Error</span><span class="sxs-lookup"><span data-stu-id="46c27-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="46c27-120">Si se producen errores durante la sincronización, el proveedor de almacenamiento llama a esta función para proporcionar detalles que se muestran en el cuadro de diálogo Enviar y recibir.</span><span class="sxs-lookup"><span data-stu-id="46c27-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="46c27-121">Hecho</span><span class="sxs-lookup"><span data-stu-id="46c27-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="46c27-122">El proveedor de almacenamiento llama a esta función para informar Outlook que se ha completado la sincronización.</span><span class="sxs-lookup"><span data-stu-id="46c27-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46c27-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="46c27-123">See also</span></span>



[<span data-ttu-id="46c27-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="46c27-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="46c27-125">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="46c27-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

