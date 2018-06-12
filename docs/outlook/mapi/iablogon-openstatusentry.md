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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: e693e1c3d6cb975a3a329e15c0b1a6d08817461a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817101"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="4a62f-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="4a62f-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="4a62f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a62f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a62f-105">Se abre el objeto de estado del proveedor.</span><span class="sxs-lookup"><span data-stu-id="4a62f-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="4a62f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a62f-106">Parameters</span></span>

 <span data-ttu-id="4a62f-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4a62f-107">_lpInterface_</span></span>
  
> <span data-ttu-id="4a62f-108">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se debe utilizar para tener acceso al objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="4a62f-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="4a62f-109">Pasando NULL devuelve la interfaz del objeto estándar, [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="4a62f-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="4a62f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4a62f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="4a62f-111">[entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="4a62f-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="4a62f-112">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="4a62f-112">The following flag can be set:</span></span>
    
<span data-ttu-id="4a62f-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4a62f-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="4a62f-114">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4a62f-114">Requests read/write permission.</span></span> <span data-ttu-id="4a62f-115">De forma predeterminada, los objetos se abren con acceso de solo lectura y los autores de llamadas no deben asumir que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4a62f-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="4a62f-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="4a62f-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="4a62f-117">[out] Un puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="4a62f-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="4a62f-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="4a62f-118">_lppEntry_</span></span>
  
> <span data-ttu-id="4a62f-119">[out] Un puntero a un puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="4a62f-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4a62f-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a62f-120">Return value</span></span>

<span data-ttu-id="4a62f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="4a62f-121">S_OK</span></span> 
  
> <span data-ttu-id="4a62f-122">La llamada se ha realizado correctamente y se ha abierto el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="4a62f-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4a62f-123">Notas</span><span class="sxs-lookup"><span data-stu-id="4a62f-123">Remarks</span></span>

<span data-ttu-id="4a62f-124">Los proveedores de la libreta de direcciones implementan el método **OpenStatusEntry** para conceder acceso a su objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="4a62f-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="4a62f-125">Todos los proveedores de libreta de direcciones son necesarios para implementar un objeto de estado que admite, como mínimo, el método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="4a62f-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="4a62f-126">Para obtener más información, vea [Implementación de objeto de estado](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="4a62f-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4a62f-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="4a62f-127">See also</span></span>



[<span data-ttu-id="4a62f-128">IMAPIStatus: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4a62f-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="4a62f-129">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="4a62f-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="4a62f-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="4a62f-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="4a62f-131">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a62f-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

