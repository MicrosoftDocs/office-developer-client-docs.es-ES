---
title: IMAPISupportNewUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a38f7ea475f8a5cbad4f1cc295c3e2550ea8cd66
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407000"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="4a4e6-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="4a4e6-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="4a4e6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a4e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a4e6-105">Crea una nueva estructura [MAPIUID](mapiuid.md) para usarla como identificador único.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="4a4e6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4a4e6-106">Parameters</span></span>

 <span data-ttu-id="4a4e6-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="4a4e6-107">_lpMuid_</span></span>
  
> <span data-ttu-id="4a4e6-108">Un puntero a la nueva estructura **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="4a4e6-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4a4e6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a4e6-109">Return value</span></span>

<span data-ttu-id="4a4e6-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="4a4e6-110">S_OK</span></span> 
  
> <span data-ttu-id="4a4e6-111">Se ha creado la nueva estructura **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="4a4e6-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4a4e6-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a4e6-112">Remarks</span></span>

<span data-ttu-id="4a4e6-113">El método **IMAPISupport:: NewUID** se implementa para todos los objetos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="4a4e6-114">Los proveedores de servicios y los servicios de mensajes llaman a **NewUID** cada vez que necesitan generar un identificador único a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="4a4e6-115">Un proveedor de almacenamiento de mensajes, por ejemplo, puede llamar a **NewUID** para obtener una **MAPIUID** para colocarla en la propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de un mensaje recién creado.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4a4e6-116">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="4a4e6-116">Notes to callers</span></span>

<span data-ttu-id="4a4e6-117">No confunda la estructura **MAPIUID** que se registra en el momento de inicio de sesión con las estructuras **MAPIUID** que crea el método **NewUID** .</span><span class="sxs-lookup"><span data-stu-id="4a4e6-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="4a4e6-118">La estructura **MAPIUID** que se registra cuando se llama al método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) representa su libreta de direcciones o proveedor de almacenamiento de mensajes en MAPI y se usa para distinguir los identificadores de entrada que crean proveedores distintos.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="4a4e6-119">Esta estructura **MAPIUID** debe estar codificada de forma rígida y no obtenerse a través de una llamada a **NewUID**.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4a4e6-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="4a4e6-120">See also</span></span>



[<span data-ttu-id="4a4e6-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="4a4e6-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="4a4e6-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a4e6-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

