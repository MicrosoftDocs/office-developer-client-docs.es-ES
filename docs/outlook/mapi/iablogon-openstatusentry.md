---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 22f98e52444b17c383737bffd1685df0fb7ba8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410787"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="876e5-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="876e5-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="876e5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="876e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="876e5-105">Abre el objeto status del proveedor.</span><span class="sxs-lookup"><span data-stu-id="876e5-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="876e5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="876e5-106">Parameters</span></span>

 <span data-ttu-id="876e5-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="876e5-107">_lpInterface_</span></span>
  
> <span data-ttu-id="876e5-108">[in] Puntero al identificador de interfaz (IID) que representa la interfaz que debe usarse para obtener acceso al objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="876e5-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="876e5-109">Si se pasa NULL, se devuelve la interfaz estándar del objeto, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="876e5-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="876e5-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="876e5-110">_ulFlags_</span></span>
  
> <span data-ttu-id="876e5-111">[in] Máscara de bits de marcas que controla cómo se abre el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="876e5-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="876e5-112">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="876e5-112">The following flag can be set:</span></span>
    
<span data-ttu-id="876e5-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="876e5-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="876e5-114">Solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="876e5-114">Requests read/write permission.</span></span> <span data-ttu-id="876e5-115">De forma predeterminada, los objetos se abren con acceso de solo lectura y los autores de llamadas no deben asumir que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="876e5-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="876e5-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="876e5-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="876e5-117">[salida] Puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="876e5-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="876e5-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="876e5-118">_lppEntry_</span></span>
  
> <span data-ttu-id="876e5-119">[salida] Puntero a un puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="876e5-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="876e5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="876e5-120">Return value</span></span>

<span data-ttu-id="876e5-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="876e5-121">S_OK</span></span> 
  
> <span data-ttu-id="876e5-122">La llamada se ha realizado correctamente y se ha abierto el objeto status.</span><span class="sxs-lookup"><span data-stu-id="876e5-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="876e5-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="876e5-123">Remarks</span></span>

<span data-ttu-id="876e5-124">Los proveedores de libreta de direcciones implementan **el método OpenStatusEntry** para conceder acceso a su objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="876e5-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="876e5-125">Todos los proveedores de libreta de direcciones son necesarios para implementar un objeto de estado que admita, como mínimo, el [método IMAPIStatus::ValidateState.](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="876e5-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="876e5-126">Para obtener más información, vea [Status Object Implementation](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="876e5-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="876e5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="876e5-127">See also</span></span>



[<span data-ttu-id="876e5-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="876e5-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="876e5-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="876e5-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="876e5-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="876e5-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="876e5-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="876e5-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

