---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fd7e3b1d1284cdf4451330aabcce8fd0279ad5ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817862"
---
# <a name="ipersistmessagehandsoffmessage"></a><span data-ttu-id="ab5ec-103">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="ab5ec-103">IPersistMessage::HandsOffMessage</span></span>

  
  
<span data-ttu-id="ab5ec-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ab5ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ab5ec-105">Hace que el formulario liberar su mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="ab5ec-105">Causes the form to release its current message.</span></span>
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="ab5ec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab5ec-106">Parameters</span></span>

<span data-ttu-id="ab5ec-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ab5ec-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="ab5ec-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab5ec-108">Return value</span></span>

<span data-ttu-id="ab5ec-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab5ec-109">S_OK</span></span> 
  
> <span data-ttu-id="ab5ec-110">El mensaje fue publicado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab5ec-110">The message was successfully released.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab5ec-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab5ec-111">Remarks</span></span>

<span data-ttu-id="ab5ec-112">Transición de formularios en dos Estados de HandsOff:</span><span class="sxs-lookup"><span data-stu-id="ab5ec-112">Forms transition into two HandsOff states:</span></span>
  
- [<span data-ttu-id="ab5ec-113">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="ab5ec-113">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="ab5ec-114">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="ab5ec-114">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="ab5ec-115">Cuando un formulario está en cualquiera de estos Estados, está en el proceso que se almacena de manera permanente.</span><span class="sxs-lookup"><span data-stu-id="ab5ec-115">When a form is in either of these states, it is in the process of being stored permanently.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ab5ec-116">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="ab5ec-116">Notes to implementers</span></span>

<span data-ttu-id="ab5ec-117">Cuando un visor de formulario llama al método de **IPersistMessage::HandsOffMessage** mientras el formulario está en estado [Normal](normal-state.md) o [NoScribble](noscribble-state.md) , de forma recursiva llamada **HandsOffMessage** en cada mensaje insertado en el mensaje actual y la [ IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) método en cada objeto OLE incrustado en el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="ab5ec-117">When a form viewer calls the **IPersistMessage::HandsOffMessage** method while your form is in the [Normal](normal-state.md) or [NoScribble](noscribble-state.md) state, recursively call **HandsOffMessage** on each message embedded in the current message and the [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method on each OLE object embedded in the current message.</span></span> <span data-ttu-id="ab5ec-118">A continuación, liberar el mensaje actual y todos los mensajes y objetos OLE incrustados.</span><span class="sxs-lookup"><span data-stu-id="ab5ec-118">Then release the current message and all embedded messages and OLE objects.</span></span> <span data-ttu-id="ab5ec-119">Si el formulario se encontraba en el estado Normal, realizar la transición al estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="ab5ec-119">If your form was in the Normal state, transition to the HandsOffFromNormal state.</span></span> <span data-ttu-id="ab5ec-120">Si el formulario se encontraba en el estado de NoScribble, realizar la transición al estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="ab5ec-120">If your form was in the NoScribble state, transition to the HandsOffAfterSave state.</span></span> <span data-ttu-id="ab5ec-121">Después de una transición correcta, llamar al método [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del mensaje y devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="ab5ec-121">After a successful transition, call the message's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method and return S_OK.</span></span> 
  
<span data-ttu-id="ab5ec-122">Cuando un visor de formulario llama a **HandsOffMessage** mientras el formulario está en cualquiera de los Estados de HandsOff, devolver E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="ab5ec-122">When a form viewer calls **HandsOffMessage** while your form is in either of the HandsOff states, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="ab5ec-123">Para obtener más información acerca de los diferentes Estados de un formulario, vea [Estados de formulario](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="ab5ec-123">For more information about the different states of a form, see [Form States](form-states.md).</span></span> <span data-ttu-id="ab5ec-124">Para obtener más información acerca de cómo trabajar con el estado HandsOff de objetos de almacenamiento, vea el método [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ab5ec-124">For more information about how to work with the HandsOff state of storage objects, see the [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab5ec-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab5ec-125">See also</span></span>



[<span data-ttu-id="ab5ec-126">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ab5ec-126">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="ab5ec-127">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="ab5ec-127">Form States</span></span>](form-states.md)

