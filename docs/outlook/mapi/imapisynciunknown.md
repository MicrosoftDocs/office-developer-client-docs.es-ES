---
title: IUnknown IMAPISync
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
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341282"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="52b92-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52b92-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="52b92-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52b92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52b92-105">Proporciona un mecanismo para sincronizar el correo electrónico en lugar de usar la API de transporte.</span><span class="sxs-lookup"><span data-stu-id="52b92-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="52b92-106">Esta interfaz se expone en un objeto Store.</span><span class="sxs-lookup"><span data-stu-id="52b92-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="52b92-107">Mediante esta interfaz y [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), un proveedor de transporte puede proporcionar un mejor progreso y mensajes de error que los que aparecen en el cuadro de diálogo de envío y recepción de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="52b92-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="52b92-108">La bandeja de salida sigue en el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="52b92-108">The outbox is still in the default store.</span></span> <span data-ttu-id="52b92-109">Outlook seguirá usando las API de transporte para enviar correo, ya que el mensaje saliente no puede estar en el almacén externo.</span><span class="sxs-lookup"><span data-stu-id="52b92-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52b92-110">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="52b92-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="52b92-111">Proveedores de almacenamiento y transporte</span><span class="sxs-lookup"><span data-stu-id="52b92-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="52b92-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="52b92-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="52b92-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="52b92-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="52b92-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="52b92-114">Called by:</span></span>  <br/> |<span data-ttu-id="52b92-115">Proveedores de almacenamiento y transporte</span><span class="sxs-lookup"><span data-stu-id="52b92-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="52b92-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="52b92-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="52b92-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="52b92-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="52b92-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="52b92-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="52b92-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="52b92-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="52b92-120">Lo implementan los proveedores de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="52b92-120">Implemented by message store providers.</span></span> <span data-ttu-id="52b92-121">Este método es invocado por Outlook 2010 y Outlook 2013 para iniciar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="52b92-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52b92-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="52b92-122">See also</span></span>



[<span data-ttu-id="52b92-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52b92-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="52b92-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="52b92-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

