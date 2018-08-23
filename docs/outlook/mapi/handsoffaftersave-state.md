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
ms.openlocfilehash: 274e7206171e1874e3625896952f861d25f3b382
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564538"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="c119b-103">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="c119b-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="c119b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c119b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c119b-105">El estado de HandsOffAfterSave es parte del proceso de guardar el contenido de un formulario en un almacenamiento permanente.</span><span class="sxs-lookup"><span data-stu-id="c119b-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="c119b-106">En este estado, el objeto de formulario debe evitar realizar cambios en las copias en memoria de los valores de las propiedades del mensaje, porque puede que no haya otra oportunidad para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="c119b-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="c119b-107">La siguiente tabla describe las transiciones permitidas desde el estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="c119b-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="c119b-108">**IPersistMessage (método)**</span><span class="sxs-lookup"><span data-stu-id="c119b-108">**IPersistMessage method**</span></span>|<span data-ttu-id="c119b-109">**Acción**</span><span class="sxs-lookup"><span data-stu-id="c119b-109">**Action**</span></span>|<span data-ttu-id="c119b-110">**Nuevo estado**</span><span class="sxs-lookup"><span data-stu-id="c119b-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c119b-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ nulo)</span><span class="sxs-lookup"><span data-stu-id="c119b-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="c119b-112">Abrir objetos incrustados.</span><span class="sxs-lookup"><span data-stu-id="c119b-112">Open any embedded objects.</span></span> <span data-ttu-id="c119b-113">Los datos en el mensaje que se almacenan en _pMessage_ se garantiza que será el mismo que el mensaje en la llamada [IPersistMessage::Save](ipersistmessage-save.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="c119b-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="c119b-114">Si se realiza correctamente la llamada **SaveCompleted** , especifique el estado Normal.</span><span class="sxs-lookup"><span data-stu-id="c119b-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="c119b-115">En caso contrario, Establece el último error a E_OUTOFMEMORY y permanecer en el estado de HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="c119b-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="c119b-116">[Normal](normal-state.md) o HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="c119b-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="c119b-117">**IPersistMessage::SaveCompleted** (_pMessage ==_ nulo)</span><span class="sxs-lookup"><span data-stu-id="c119b-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="c119b-118">Establece el último error E_INVALIDARG o E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="c119b-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="c119b-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="c119b-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="c119b-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Guardar**o [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="c119b-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="c119b-121">Establece el último error y devolver E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="c119b-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="c119b-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="c119b-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="c119b-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="c119b-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="c119b-124">Cargar el objeto de formulario con datos desde el mensaje de destino.</span><span class="sxs-lookup"><span data-stu-id="c119b-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="c119b-125">Esta llamada puede producirse cuando el objeto de formulario se va al mensaje siguiente o anterior en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c119b-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="c119b-126">Importance</span><span class="sxs-lookup"><span data-stu-id="c119b-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="c119b-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c119b-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="c119b-128">Devolver el último error.</span><span class="sxs-lookup"><span data-stu-id="c119b-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="c119b-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="c119b-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="c119b-130">Otros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos o métodos de otras interfaces</span><span class="sxs-lookup"><span data-stu-id="c119b-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="c119b-131">Establece el último error y devolver E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="c119b-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="c119b-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="c119b-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c119b-133">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c119b-133">See also</span></span>



[<span data-ttu-id="c119b-134">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="c119b-134">Form States</span></span>](form-states.md)

