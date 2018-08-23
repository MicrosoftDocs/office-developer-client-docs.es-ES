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
ms.openlocfilehash: df842e633f1586d6d77441126d51b2ce44ec3beb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589073"
---
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="e3439-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="e3439-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="e3439-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3439-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3439-105">Registra una estructura [MAPIUID](mapiuid.md) que representa el proveedor de servicios de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="e3439-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e3439-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3439-106">Parameters</span></span>

 <span data-ttu-id="e3439-107">_lpProviderID_</span><span class="sxs-lookup"><span data-stu-id="e3439-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="e3439-108">[entrada] Un puntero a la estructura **MAPIUID** que identifica el proveedor de almacenamiento de mensaje o de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e3439-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="e3439-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e3439-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e3439-110">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e3439-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e3439-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3439-111">Return value</span></span>

<span data-ttu-id="e3439-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3439-112">S_OK</span></span> 
  
> <span data-ttu-id="e3439-113">La estructura **MAPIUID** se ha registrado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e3439-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e3439-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3439-114">Remarks</span></span>

<span data-ttu-id="e3439-115">El método **IMAPISupport::SetProviderUID** se implementa para dirección libreta de direcciones y el mensaje de proveedor compatibilidad con objetos de almacén.</span><span class="sxs-lookup"><span data-stu-id="e3439-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="e3439-116">Estos proveedores de llamar a **SetProviderUID** para registrar un identificador único que se describen en la estructura **MAPIUID** que señala a _lpProviderID_.</span><span class="sxs-lookup"><span data-stu-id="e3439-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="e3439-117">Proveedores de incluyen este identificador en todos los identificadores de entrada que se crean.</span><span class="sxs-lookup"><span data-stu-id="e3439-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="e3439-118">MAPI utiliza la estructura **MAPIUID** cuando envían los mensajes salientes a la cola MAPI y para determinar el proveedor adecuado para el tratamiento de las solicitudes de cliente.</span><span class="sxs-lookup"><span data-stu-id="e3439-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="e3439-119">Por ejemplo, cuando un cliente llama al método de [IMAPISession::OpenEntry](imapisession-openentry.md) , MAPI examina la parte **MAPIUID** del identificador de entrada, asigna al proveedor de que se pasa a **SetProviderUID**y llama a su proveedor **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="e3439-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e3439-120">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="e3439-120">Notes to callers</span></span>

<span data-ttu-id="e3439-121">Llamar a **SetProviderUID** en tiempo de inicio de sesión para registrar la estructura **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="e3439-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="e3439-122">MAPI permite dirección libreta de direcciones y el mensaje de los proveedores de almacén registrar varios identificadores.</span><span class="sxs-lookup"><span data-stu-id="e3439-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="e3439-123">Cuando realiza varias llamadas a **SetProviderUID**, agrega siempre la estructura **MAPIUID** a conjunto del proveedor de estructuras **MAPIUID** , incluso si la **MAPIUID** es un duplicado.</span><span class="sxs-lookup"><span data-stu-id="e3439-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="e3439-124">**SetProviderUID** no se puede quitar un **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="e3439-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e3439-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e3439-125">See also</span></span>



[<span data-ttu-id="e3439-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e3439-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="e3439-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3439-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

