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
ms.openlocfilehash: 3d45c4722b6a0200ea3937ba606da0af5c793df2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581856"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="91f27-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="91f27-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="91f27-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91f27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91f27-105">Recupera un valor que indica si el control de botón está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="91f27-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="91f27-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="91f27-106">Parameters</span></span>

 <span data-ttu-id="91f27-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="91f27-107">_ulFlags_</span></span>
  
> <span data-ttu-id="91f27-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="91f27-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="91f27-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="91f27-109">_lpulState_</span></span>
  
> <span data-ttu-id="91f27-110">[out] Un puntero a un valor que indica el estado del control de botón.</span><span class="sxs-lookup"><span data-stu-id="91f27-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="91f27-111">Puede devolver uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="91f27-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="91f27-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="91f27-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="91f27-113">El control botón está deshabilitado y no se puede hacer clic en ella.</span><span class="sxs-lookup"><span data-stu-id="91f27-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="91f27-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="91f27-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="91f27-115">El control botón está habilitado y se puede hacer clic.</span><span class="sxs-lookup"><span data-stu-id="91f27-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="91f27-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91f27-116">Return value</span></span>

<span data-ttu-id="91f27-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="91f27-117">S_OK</span></span> 
  
> <span data-ttu-id="91f27-118">El estado del control de botón se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="91f27-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91f27-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="91f27-119">Remarks</span></span>

<span data-ttu-id="91f27-120">Proveedores de servicios de implementan el método **IMAPIControl::GetState** para proporcionar MAPI con el estado de un control de botón.</span><span class="sxs-lookup"><span data-stu-id="91f27-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="91f27-121">Si el botón está habilitado, puede responder a un clic del mouse o una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="91f27-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="91f27-122">Si está deshabilitada, el botón aparece atenuado y no responde a un clic del mouse o una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="91f27-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="91f27-123">Para obtener más información acerca de cómo implementar **GetState** y la otra [IMAPIControl: IUnknown](imapicontroliunknown.md) métodos, vea [Implementación de objeto de Control](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="91f27-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="91f27-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="91f27-124">See also</span></span>



[<span data-ttu-id="91f27-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="91f27-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="91f27-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="91f27-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

