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
# <a name="handsoffaftersave-state"></a><span data-ttu-id="56671-103">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="56671-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="56671-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56671-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56671-105">El estado HandsOffAfterSave forma parte del proceso de guardar el contenido de un formulario en un almacenamiento permanente.</span><span class="sxs-lookup"><span data-stu-id="56671-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="56671-106">Cuando se encuentra en este estado, el objeto Form debe abstenerse de realizar cambios en las copias en memoria de los valores de las propiedades del mensaje, porque puede que no haya otra oportunidad para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="56671-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="56671-107">En la tabla siguiente se describen las transiciones permitidas desde el estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="56671-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="56671-108">**Método IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="56671-108">**IPersistMessage method**</span></span>|<span data-ttu-id="56671-109">**Acción**</span><span class="sxs-lookup"><span data-stu-id="56671-109">**Action**</span></span>|<span data-ttu-id="56671-110">**Nuevo estado**</span><span class="sxs-lookup"><span data-stu-id="56671-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="56671-111">[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ null)</span><span class="sxs-lookup"><span data-stu-id="56671-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="56671-112">Abra los objetos incrustados.</span><span class="sxs-lookup"><span data-stu-id="56671-112">Open any embedded objects.</span></span> <span data-ttu-id="56671-113">Se garantiza que los datos del mensaje almacenados en _pMessage_ son los mismos que los del mensaje de la llamada anterior a [IPersistMessage:: Save](ipersistmessage-save.md) .</span><span class="sxs-lookup"><span data-stu-id="56671-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="56671-114">Si la llamada **SaveCompleted** se realiza correctamente, escriba el estado normal.</span><span class="sxs-lookup"><span data-stu-id="56671-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="56671-115">De lo contrario, establezca el último error en E_OUTOFMEMORY y manténgase en el estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="56671-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="56671-116">[Normal](normal-state.md) o HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="56671-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="56671-117">**IPersistMessage:: SaveCompleted** (_pMessage = =_ null)</span><span class="sxs-lookup"><span data-stu-id="56671-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="56671-118">Establezca el último error en E_INVALIDARG o E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="56671-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="56671-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="56671-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="56671-120">[IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**o [IPersistMessage:: InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="56671-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="56671-121">Establezca el último error en y devuelva E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="56671-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="56671-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="56671-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="56671-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="56671-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="56671-124">Cargue el objeto de formulario con datos del mensaje de destino.</span><span class="sxs-lookup"><span data-stu-id="56671-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="56671-125">Esta llamada puede producirse cuando el objeto de formulario va al mensaje siguiente o anterior en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="56671-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="56671-126">Normal</span><span class="sxs-lookup"><span data-stu-id="56671-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="56671-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="56671-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="56671-128">Devolver el último error.</span><span class="sxs-lookup"><span data-stu-id="56671-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="56671-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="56671-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="56671-130">Otros [IPersistMessage:](ipersistmessageiunknown.md) métodos o métodos IUnknown de otras interfaces</span><span class="sxs-lookup"><span data-stu-id="56671-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="56671-131">Establezca el último error en y devuelva E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="56671-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="56671-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="56671-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="56671-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="56671-133">See also</span></span>



[<span data-ttu-id="56671-134">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="56671-134">Form States</span></span>](form-states.md)

