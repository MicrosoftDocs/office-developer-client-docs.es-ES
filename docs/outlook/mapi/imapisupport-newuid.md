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
ms.openlocfilehash: 14be41c21244abe8c54261a95a410828c973d66b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817517"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="8c470-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="8c470-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="8c470-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c470-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c470-105">Crea una nueva estructura [MAPIUID](mapiuid.md) que se utilizará como un identificador único.</span><span class="sxs-lookup"><span data-stu-id="8c470-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="8c470-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c470-106">Parameters</span></span>

 <span data-ttu-id="8c470-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="8c470-107">_lpMuid_</span></span>
  
> <span data-ttu-id="8c470-108">Un puntero a la nueva estructura **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="8c470-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8c470-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c470-109">Return value</span></span>

<span data-ttu-id="8c470-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="8c470-110">S_OK</span></span> 
  
> <span data-ttu-id="8c470-111">Se ha creado la nueva estructura **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="8c470-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8c470-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c470-112">Remarks</span></span>

<span data-ttu-id="8c470-113">El método **IMAPISupport::NewUID** se implementa para todos los objetos de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="8c470-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="8c470-114">Proveedores de servicio y servicios de mensajes de llamada **NewUID** cada vez que se necesitan para generar un identificador único a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="8c470-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="8c470-115">Un mensaje de almacenar proveedor, por ejemplo, puede llamar a **NewUID** para obtener un **MAPIUID** para poner en la propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de un mensaje recién creado.</span><span class="sxs-lookup"><span data-stu-id="8c470-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="8c470-116">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="8c470-116">Notes to callers</span></span>

<span data-ttu-id="8c470-117">Es importante no confundir la estructura **MAPIUID** que registrar en tiempo de inicio de sesión con las estructuras **MAPIUID** que crea el método **NewUID** .</span><span class="sxs-lookup"><span data-stu-id="8c470-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="8c470-118">La estructura **MAPIUID** que registrar cuando se llama al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) representa la libreta de direcciones o mensaje de proveedor MAPI de almacén y se usa para distinguir los identificadores de entrada que crean proveedores diferentes.</span><span class="sxs-lookup"><span data-stu-id="8c470-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="8c470-119">Esta estructura **MAPIUID** debe ser codificado de forma rígida y no se obtienen a través de una llamada a **NewUID**.</span><span class="sxs-lookup"><span data-stu-id="8c470-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8c470-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c470-120">See also</span></span>



[<span data-ttu-id="8c470-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8c470-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="8c470-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c470-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

