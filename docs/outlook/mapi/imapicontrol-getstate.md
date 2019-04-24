---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f477c617533d66fc129c7192c9f86bb8a46afbb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280283"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="cca86-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="cca86-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="cca86-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cca86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cca86-105">Recupera un valor que indica si el control de botón está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="cca86-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="cca86-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cca86-106">Parameters</span></span>

 <span data-ttu-id="cca86-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cca86-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cca86-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cca86-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cca86-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="cca86-109">_lpulState_</span></span>
  
> <span data-ttu-id="cca86-110">contempla Puntero a un valor que indica el estado del control de botón.</span><span class="sxs-lookup"><span data-stu-id="cca86-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="cca86-111">Se puede devolver uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="cca86-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="cca86-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="cca86-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="cca86-113">El control botón está deshabilitado y no se puede hacer clic en él.</span><span class="sxs-lookup"><span data-stu-id="cca86-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="cca86-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="cca86-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="cca86-115">El control botón está habilitado y se puede hacer clic en él.</span><span class="sxs-lookup"><span data-stu-id="cca86-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cca86-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cca86-116">Return value</span></span>

<span data-ttu-id="cca86-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="cca86-117">S_OK</span></span> 
  
> <span data-ttu-id="cca86-118">El estado del control de botón se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cca86-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cca86-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cca86-119">Remarks</span></span>

<span data-ttu-id="cca86-120">Los proveedores de servicios implementan el método **IMAPIControl:: GetState** para proporcionar MAPI con el estado de un control de botón.</span><span class="sxs-lookup"><span data-stu-id="cca86-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="cca86-121">Si el botón está habilitado, puede responder a un clic del mouse o a una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="cca86-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="cca86-122">Si está deshabilitada, el botón aparece atenuado y no responde a un clic del mouse o a una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="cca86-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="cca86-123">Para obtener más información sobre cómo implementar **GetState** y los otros [IMAPIControl: métodos IUnknown](imapicontroliunknown.md) , vea [control](control-object-implementation.md)de la implementación de objetos.</span><span class="sxs-lookup"><span data-stu-id="cca86-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cca86-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="cca86-124">See also</span></span>



[<span data-ttu-id="cca86-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="cca86-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="cca86-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cca86-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

