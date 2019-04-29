---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtiene la siguiente cuenta del enumerador.
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405992"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="49b18-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="49b18-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="49b18-104">Obtiene la siguiente cuenta del enumerador.</span><span class="sxs-lookup"><span data-stu-id="49b18-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="49b18-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="49b18-105">Quick info</span></span>

<span data-ttu-id="49b18-106">Consulte [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="49b18-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="49b18-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="49b18-107">Parameters</span></span>

<span data-ttu-id="49b18-108">_ppunk_</span><span class="sxs-lookup"><span data-stu-id="49b18-108">_ppunk_</span></span>
  
> <span data-ttu-id="49b18-109">a Un puntero a una interfaz **IUnknown** que el cliente puede consultar para obtener una interfaz [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="49b18-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="49b18-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="49b18-110">Return values</span></span>

|<span data-ttu-id="49b18-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="49b18-111">**HRESULT**</span></span>|<span data-ttu-id="49b18-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="49b18-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="49b18-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="49b18-113">S_OK</span></span>  <br/> |<span data-ttu-id="49b18-114">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="49b18-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="49b18-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="49b18-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="49b18-116">El enumerador ha alcanzado el final.</span><span class="sxs-lookup"><span data-stu-id="49b18-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49b18-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49b18-117">Remarks</span></span>

<span data-ttu-id="49b18-118">La interfaz especificada por *ppunk* hereda de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="49b18-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="49b18-119">El cliente puede consultar esta interfaz (mediante **IUnknown:: QueryInterface**) para obtener un puntero a una interfaz **IOlkAccount** y obtener o establecer información de esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="49b18-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="49b18-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="49b18-120">See also</span></span>

- [<span data-ttu-id="49b18-121">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="49b18-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="49b18-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="49b18-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="49b18-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="49b18-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="49b18-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="49b18-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

