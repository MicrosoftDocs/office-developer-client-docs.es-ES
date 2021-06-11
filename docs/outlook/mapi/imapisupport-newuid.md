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
# <a name="imapisupportnewuid"></a><span data-ttu-id="113d7-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="113d7-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="113d7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="113d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="113d7-105">Crea una nueva [estructura MAPIUID](mapiuid.md) que se usará como identificador único.</span><span class="sxs-lookup"><span data-stu-id="113d7-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="113d7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="113d7-106">Parameters</span></span>

 <span data-ttu-id="113d7-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="113d7-107">_lpMuid_</span></span>
  
> <span data-ttu-id="113d7-108">Puntero a la nueva **estructura MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="113d7-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="113d7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="113d7-109">Return value</span></span>

<span data-ttu-id="113d7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="113d7-110">S_OK</span></span> 
  
> <span data-ttu-id="113d7-111">Se **creó la nueva estructura MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="113d7-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="113d7-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="113d7-112">Remarks</span></span>

<span data-ttu-id="113d7-113">El **método IMAPISupport::NewUID** se implementa para todos los objetos de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="113d7-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="113d7-114">Los proveedores de servicios y servicios de mensajes llaman a **NewUID** siempre que necesiten generar un identificador único a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="113d7-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="113d7-115">Un proveedor de almacén de mensajes, por ejemplo, puede llamar a **NewUID** para obtener **un MAPIUID** para colocar la propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de un mensaje recién creado.</span><span class="sxs-lookup"><span data-stu-id="113d7-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="113d7-116">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="113d7-116">Notes to callers</span></span>

<span data-ttu-id="113d7-117">No confunda la estructura **MAPIUID** que se registra durante el inicio de sesión con las estructuras **MAPIUID** que **crea el método NewUID.**</span><span class="sxs-lookup"><span data-stu-id="113d7-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="113d7-118">La estructura **MAPIUID** que se registra al llamar al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) representa la libreta de direcciones o el proveedor del almacén de mensajes a MAPI y se usa para distinguir los identificadores de entrada que crean los distintos proveedores.</span><span class="sxs-lookup"><span data-stu-id="113d7-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="113d7-119">Esta **estructura MAPIUID** debe codificarse de forma sólida y no obtenerse a través de una llamada a **NewUID**.</span><span class="sxs-lookup"><span data-stu-id="113d7-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="113d7-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="113d7-120">See also</span></span>



[<span data-ttu-id="113d7-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="113d7-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="113d7-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="113d7-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

