---
title: Estado HandsOffFromNormal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d0b7baf4ab17d12145170961a43ca4be252146a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816962"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="7b5db-103">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7b5db-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="7b5db-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b5db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b5db-105">El estado de HandsOffFromNormal es muy similar al estado [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5db-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="7b5db-106">Forma parte del proceso de guardar el contenido de un formulario en un almacenamiento permanente.</span><span class="sxs-lookup"><span data-stu-id="7b5db-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="7b5db-107">En este estado, el objeto de formulario debe evitar realizar cambios en las copias en memoria de los valores de las propiedades del mensaje, porque puede que no haya otra oportunidad para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="7b5db-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="7b5db-108">La siguiente tabla describe las transiciones permitidas desde el estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="7b5db-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="7b5db-109">IPersistMessage ** (método) **</span><span class="sxs-lookup"><span data-stu-id="7b5db-109">****IPersistMessage** method**</span></span>|<span data-ttu-id="7b5db-110">**Acción**</span><span class="sxs-lookup"><span data-stu-id="7b5db-110">**Action**</span></span>|<span data-ttu-id="7b5db-111">**Nuevo estado**</span><span class="sxs-lookup"><span data-stu-id="7b5db-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7b5db-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ nulo)</span><span class="sxs-lookup"><span data-stu-id="7b5db-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="7b5db-113">Reemplazar el mensaje del objeto de mensaje con _pMessage_, que es el sustituto para el mensaje revocado por la llamada anterior a [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span><span class="sxs-lookup"><span data-stu-id="7b5db-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="7b5db-114">Los datos en el nuevo mensaje se garantiza que será el mismo que en el mensaje revocado.</span><span class="sxs-lookup"><span data-stu-id="7b5db-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="7b5db-115">No se debe marcar el mensaje como limpio, ni debe llamarse [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) después de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="7b5db-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="7b5db-116">Si se realiza correctamente la llamada **SaveCompleted** , especifique el estado [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5db-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="7b5db-117">De lo contrario, permanecer en el estado de HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="7b5db-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="7b5db-118">Normal o HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7b5db-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="7b5db-119">**IPersistMessage::SaveCompleted** (_pMessage ==_ nulo)</span><span class="sxs-lookup"><span data-stu-id="7b5db-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="7b5db-120">Establece el último error a E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="7b5db-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="7b5db-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7b5db-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="7b5db-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)o [IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="7b5db-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="7b5db-123">Establece el último error a E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="7b5db-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="7b5db-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7b5db-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="7b5db-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7b5db-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="7b5db-126">Devolver el último error.</span><span class="sxs-lookup"><span data-stu-id="7b5db-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="7b5db-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7b5db-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="7b5db-128">Otros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos o métodos de otras interfaces</span><span class="sxs-lookup"><span data-stu-id="7b5db-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="7b5db-129">Establece el último error a E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="7b5db-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="7b5db-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="7b5db-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b5db-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b5db-131">See also</span></span>



[<span data-ttu-id="7b5db-132">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="7b5db-132">Form States</span></span>](form-states.md)

