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
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426474"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="50b1c-103">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="50b1c-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="50b1c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50b1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50b1c-105">El estado HandsOffFromNormal es muy similar al [estado HandsOffAfterSave.](handsoffaftersave-state.md)</span><span class="sxs-lookup"><span data-stu-id="50b1c-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="50b1c-106">Forma parte del proceso de guardar el contenido de un formulario en un almacenamiento permanente.</span><span class="sxs-lookup"><span data-stu-id="50b1c-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="50b1c-107">Cuando se encuentra en este estado, el objeto form debe abstenerse de realizar cambios en las copias en memoria de los valores de las propiedades del mensaje, ya que es posible que no haya otra oportunidad de guardar esos cambios.</span><span class="sxs-lookup"><span data-stu-id="50b1c-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="50b1c-108">En la tabla siguiente se describen las transiciones permitidas desde el estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="50b1c-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="50b1c-109">Método IPersistMessage\*\*</span><span class="sxs-lookup"><span data-stu-id="50b1c-109">\*\*\*\*IPersistMessage\*\* method\*\*</span></span>|<span data-ttu-id="50b1c-110">**Action**</span><span class="sxs-lookup"><span data-stu-id="50b1c-110">**Action**</span></span>|<span data-ttu-id="50b1c-111">**Nuevo estado**</span><span class="sxs-lookup"><span data-stu-id="50b1c-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="50b1c-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span><span class="sxs-lookup"><span data-stu-id="50b1c-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="50b1c-113">Reemplace el mensaje del objeto message por  _pMessage_, que es el reemplazo del mensaje revocado por la llamada anterior a [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span><span class="sxs-lookup"><span data-stu-id="50b1c-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="50b1c-114">Se garantiza que los datos del nuevo mensaje sean los mismos que en el mensaje revocado.</span><span class="sxs-lookup"><span data-stu-id="50b1c-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="50b1c-115">El mensaje no debe marcarse como limpio ni se debe llamar a [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) después de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="50b1c-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="50b1c-116">Si la **llamada SaveCompleted** se realiza correctamente, escriba el [estado Normal.](normal-state.md)</span><span class="sxs-lookup"><span data-stu-id="50b1c-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="50b1c-117">De lo contrario, permanezca en el estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="50b1c-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="50b1c-118">Normal o HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="50b1c-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="50b1c-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="50b1c-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="50b1c-120">Establezca el último error en E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="50b1c-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="50b1c-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="50b1c-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="50b1c-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)o [IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="50b1c-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="50b1c-123">Establezca el último error en E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="50b1c-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="50b1c-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="50b1c-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="50b1c-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="50b1c-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="50b1c-126">Devuelve el último error.</span><span class="sxs-lookup"><span data-stu-id="50b1c-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="50b1c-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="50b1c-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="50b1c-128">Otros [métodos o métodos IPersistMessage: IUnknown](ipersistmessageiunknown.md) de otras interfaces</span><span class="sxs-lookup"><span data-stu-id="50b1c-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="50b1c-129">Establezca el último error en E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="50b1c-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="50b1c-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="50b1c-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50b1c-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="50b1c-131">See also</span></span>



[<span data-ttu-id="50b1c-132">Estados del formulario</span><span class="sxs-lookup"><span data-stu-id="50b1c-132">Form States</span></span>](form-states.md)

