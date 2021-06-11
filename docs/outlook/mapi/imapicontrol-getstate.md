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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419012"
---
# <a name="imapicontrolgetstate"></a><span data-ttu-id="8448b-103">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="8448b-103">IMAPIControl::GetState</span></span>

  
  
<span data-ttu-id="8448b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8448b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8448b-105">Recupera un valor que indica si el control de botón está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8448b-105">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a><span data-ttu-id="8448b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8448b-106">Parameters</span></span>

 <span data-ttu-id="8448b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8448b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8448b-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8448b-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8448b-109">_lpulState_</span><span class="sxs-lookup"><span data-stu-id="8448b-109">_lpulState_</span></span>
  
> <span data-ttu-id="8448b-110">[salida] Puntero a un valor que indica el estado del control de botón.</span><span class="sxs-lookup"><span data-stu-id="8448b-110">[out] A pointer to a value that indicates the state of the button control.</span></span> <span data-ttu-id="8448b-111">Se puede devolver uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8448b-111">One of the following values can be returned:</span></span>
    
<span data-ttu-id="8448b-112">MAPI_DISABLED</span><span class="sxs-lookup"><span data-stu-id="8448b-112">MAPI_DISABLED</span></span> 
  
> <span data-ttu-id="8448b-113">El control de botón está deshabilitado y no se puede hacer clic en el botón.</span><span class="sxs-lookup"><span data-stu-id="8448b-113">The button control is disabled and cannot be clicked.</span></span> 
    
<span data-ttu-id="8448b-114">MAPI_ENABLED</span><span class="sxs-lookup"><span data-stu-id="8448b-114">MAPI_ENABLED</span></span> 
  
> <span data-ttu-id="8448b-115">El control de botón está habilitado y se puede hacer clic en el botón.</span><span class="sxs-lookup"><span data-stu-id="8448b-115">The button control is enabled and can be clicked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8448b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8448b-116">Return value</span></span>

<span data-ttu-id="8448b-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="8448b-117">S_OK</span></span> 
  
> <span data-ttu-id="8448b-118">El estado del control de botón se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8448b-118">The state of the button control was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8448b-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8448b-119">Remarks</span></span>

<span data-ttu-id="8448b-120">Los proveedores de servicios implementan **el método IMAPIControl::GetState** para proporcionar MAPI con el estado de un control de botón.</span><span class="sxs-lookup"><span data-stu-id="8448b-120">Service providers implement the **IMAPIControl::GetState** method to provide MAPI with the state of a button control.</span></span> <span data-ttu-id="8448b-121">Si el botón está habilitado, puede responder a un clic del mouse o a una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="8448b-121">If the button is enabled, it can respond to a mouse click or key press.</span></span> <span data-ttu-id="8448b-122">Si está deshabilitado, el botón aparece atenuado y no responde a un clic del mouse ni a una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="8448b-122">If it is disabled, the button appears dimmed and does not respond to a mouse click or key press.</span></span> 
  
<span data-ttu-id="8448b-123">Para obtener más información acerca de cómo implementar **GetState y** los otros métodos [IMAPIControl : IUnknown,](imapicontroliunknown.md) vea [Control Object Implementation](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="8448b-123">For more information about how to implement **GetState** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8448b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8448b-124">See also</span></span>



[<span data-ttu-id="8448b-125">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="8448b-125">IMAPIControl::Activate</span></span>](imapicontrol-activate.md)
  
[<span data-ttu-id="8448b-126">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8448b-126">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

