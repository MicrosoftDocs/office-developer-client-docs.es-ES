---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437542"
---
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="bcacd-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="bcacd-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="bcacd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcacd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcacd-105">Registra una estructura [MAPIUID](mapiuid.md) que representa de forma única el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="bcacd-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bcacd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcacd-106">Parameters</span></span>

 <span data-ttu-id="bcacd-107">_lpProviderID_</span><span class="sxs-lookup"><span data-stu-id="bcacd-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="bcacd-108">[entrada] Puntero a la estructura **MAPIUID** que identifica la libreta de direcciones o el proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bcacd-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="bcacd-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bcacd-109">_ulFlags_</span></span>
  
> <span data-ttu-id="bcacd-110">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bcacd-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bcacd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcacd-111">Return value</span></span>

<span data-ttu-id="bcacd-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="bcacd-112">S_OK</span></span> 
  
> <span data-ttu-id="bcacd-113">La **estructura MAPIUID** se registró correctamente.</span><span class="sxs-lookup"><span data-stu-id="bcacd-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bcacd-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bcacd-114">Remarks</span></span>

<span data-ttu-id="bcacd-115">El **método IMAPISupport::SetProviderUID** se implementa para objetos de compatibilidad con la libreta de direcciones y el proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bcacd-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="bcacd-116">Estos proveedores llaman **a SetProviderUID** para registrar un identificador único descrito en la estructura **MAPIUID** a la que apunta  _lpProviderID_.</span><span class="sxs-lookup"><span data-stu-id="bcacd-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="bcacd-117">Los proveedores incluyen este identificador en todos los identificadores de entrada que crean.</span><span class="sxs-lookup"><span data-stu-id="bcacd-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="bcacd-118">MAPI usa la **estructura MAPIUID** cuando envía mensajes salientes a la cola MAPI y para determinar el proveedor adecuado para controlar las solicitudes de cliente.</span><span class="sxs-lookup"><span data-stu-id="bcacd-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="bcacd-119">Por ejemplo, cuando un cliente llama al método [IMAPISession::OpenEntry,](imapisession-openentry.md) MAPI examina la parte **MAPIUID** del identificador de entrada, la asigna al proveedor que lo pasó a **SetProviderUID** y llama a **OpenEntry** de ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="bcacd-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bcacd-120">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="bcacd-120">Notes to callers</span></span>

<span data-ttu-id="bcacd-121">Llame **a SetProviderUID** durante el inicio de sesión para registrar la **estructura MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="bcacd-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="bcacd-122">MAPI permite a los proveedores de libretas de direcciones y al almacén de mensajes registrar varios identificadores.</span><span class="sxs-lookup"><span data-stu-id="bcacd-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="bcacd-123">Cuando realiza varias llamadas a **SetProviderUID,** siempre agrega la estructura **MAPIUID** al conjunto del proveedor de estructuras **MAPIUID,** incluso si **MAPIUID** es un duplicado.</span><span class="sxs-lookup"><span data-stu-id="bcacd-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="bcacd-124">**SetProviderUID** no puede quitar **un MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="bcacd-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bcacd-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bcacd-125">See also</span></span>



[<span data-ttu-id="bcacd-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="bcacd-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="bcacd-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bcacd-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

