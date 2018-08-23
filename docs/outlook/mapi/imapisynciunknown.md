---
title: IMAPISync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8e2e7a3f9279485d862fac5bb6413b3d3eb1343e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589087"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="8a66b-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a66b-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="8a66b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a66b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a66b-105">Proporciona un mecanismo para sincronizar el correo electrónico en lugar de usar la API de transporte.</span><span class="sxs-lookup"><span data-stu-id="8a66b-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="8a66b-106">Esta interfaz se expone en un objeto de almacén.</span><span class="sxs-lookup"><span data-stu-id="8a66b-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="8a66b-107">Mediante el uso de esta interfaz y [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), un proveedor de transporte puede proporcionar un mejor progreso y mensajes de error que los que aparecen en el cuadro de diálogo de envío o recepción en Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="8a66b-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="8a66b-108">La Bandeja de salida aún está en el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8a66b-108">The outbox is still in the default store.</span></span> <span data-ttu-id="8a66b-109">Outlook seguirán usando las API de transporte para enviar correo porque no puede ser el mensaje saliente en el almacén externo.</span><span class="sxs-lookup"><span data-stu-id="8a66b-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a66b-110">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="8a66b-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="8a66b-111">Proveedores de almacenamiento y transporte</span><span class="sxs-lookup"><span data-stu-id="8a66b-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="8a66b-112">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="8a66b-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="8a66b-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="8a66b-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="8a66b-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="8a66b-114">Called by:</span></span>  <br/> |<span data-ttu-id="8a66b-115">Proveedores de almacenamiento y transporte</span><span class="sxs-lookup"><span data-stu-id="8a66b-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="8a66b-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="8a66b-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8a66b-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="8a66b-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8a66b-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="8a66b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8a66b-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="8a66b-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="8a66b-120">Implementada por los proveedores de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8a66b-120">Implemented by message store providers.</span></span> <span data-ttu-id="8a66b-121">Este método es llamado por Outlook 2010 y Outlook 2013 para iniciar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="8a66b-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a66b-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8a66b-122">See also</span></span>



[<span data-ttu-id="8a66b-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a66b-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="8a66b-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="8a66b-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

