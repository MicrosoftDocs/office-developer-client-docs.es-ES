---
title: Estado HandsOffAfterSave
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406608"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="096d0-103">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="096d0-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="096d0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="096d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="096d0-105">El estado HandsOffAfterSave forma parte del proceso de guardar el contenido de un formulario en un almacenamiento permanente.</span><span class="sxs-lookup"><span data-stu-id="096d0-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="096d0-106">Cuando se encuentra en este estado, el objeto de formulario debe evitar realizar cambios en las copias en memoria de los valores de las propiedades del mensaje, ya que es posible que no haya otra oportunidad para guardar esos cambios.</span><span class="sxs-lookup"><span data-stu-id="096d0-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="096d0-107">En la tabla siguiente se describen las transiciones permitidas desde el estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="096d0-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="096d0-108">**Método IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="096d0-108">**IPersistMessage method**</span></span>|<span data-ttu-id="096d0-109">**Acción**</span><span class="sxs-lookup"><span data-stu-id="096d0-109">**Action**</span></span>|<span data-ttu-id="096d0-110">**Nuevo estado**</span><span class="sxs-lookup"><span data-stu-id="096d0-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="096d0-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span><span class="sxs-lookup"><span data-stu-id="096d0-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="096d0-112">Abra los objetos incrustados.</span><span class="sxs-lookup"><span data-stu-id="096d0-112">Open any embedded objects.</span></span> <span data-ttu-id="096d0-113">Se garantiza que los datos del mensaje almacenado en  _pMessage_ sean los mismos que los del mensaje de la llamada [IPersistMessage::Save](ipersistmessage-save.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="096d0-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="096d0-114">Si la **llamada SaveCompleted** se realiza correctamente, escriba el estado Normal.</span><span class="sxs-lookup"><span data-stu-id="096d0-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="096d0-115">De lo contrario, establezca el último error en E_OUTOFMEMORY y permanezca en el estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="096d0-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="096d0-116">[Normal](normal-state.md) o HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="096d0-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="096d0-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="096d0-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="096d0-118">Establezca el último error en E_INVALIDARG o E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="096d0-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="096d0-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="096d0-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="096d0-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save** o [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="096d0-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="096d0-121">Establezca el último error en y devuelva E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="096d0-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="096d0-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="096d0-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="096d0-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="096d0-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="096d0-124">Cargue el objeto de formulario con datos del mensaje de destino.</span><span class="sxs-lookup"><span data-stu-id="096d0-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="096d0-125">Esta llamada puede producirse cuando el objeto de formulario va al mensaje siguiente o anterior de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="096d0-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="096d0-126">Normal</span><span class="sxs-lookup"><span data-stu-id="096d0-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="096d0-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="096d0-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="096d0-128">Devuelve el último error.</span><span class="sxs-lookup"><span data-stu-id="096d0-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="096d0-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="096d0-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="096d0-130">Otros [métodos de IPersistMessage : IUnknown](ipersistmessageiunknown.md) o de otras interfaces</span><span class="sxs-lookup"><span data-stu-id="096d0-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="096d0-131">Establezca el último error en y devuelva E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="096d0-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="096d0-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="096d0-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="096d0-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="096d0-133">See also</span></span>



[<span data-ttu-id="096d0-134">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="096d0-134">Form States</span></span>](form-states.md)

