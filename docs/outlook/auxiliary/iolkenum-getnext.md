---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtiene la cuenta siguiente en el enumerador.
ms.openlocfilehash: 496a4d787916d051c051b3a19a7113d9d50c6fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816261"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="96262-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="96262-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="96262-104">Obtiene la cuenta siguiente en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="96262-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="96262-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="96262-105">Quick info</span></span>

<span data-ttu-id="96262-106">Vea [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="96262-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="96262-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96262-107">Parameters</span></span>

<span data-ttu-id="96262-108">_ppUnk_</span><span class="sxs-lookup"><span data-stu-id="96262-108">_ppunk_</span></span>
  
> <span data-ttu-id="96262-109">[entrada] Un puntero a una interfaz **IUnknown** que el cliente puede consultar para obtener una interfaz [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="96262-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="96262-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="96262-110">Return values</span></span>

|<span data-ttu-id="96262-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="96262-111">**HRESULT**</span></span>|<span data-ttu-id="96262-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="96262-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="96262-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="96262-113">S_OK</span></span>  <br/> |<span data-ttu-id="96262-114">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="96262-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="96262-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="96262-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="96262-116">El enumerador ha llegado al final.</span><span class="sxs-lookup"><span data-stu-id="96262-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96262-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96262-117">Remarks</span></span>

<span data-ttu-id="96262-118">La interfaz especificada por *ppunk* hereda de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="96262-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="96262-119">El cliente puede consultar esta interfaz (mediante **IUnknown:: QueryInterface**) para obtener un puntero a una interfaz **IOlkAccount** y obtener o establecer la información de esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="96262-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="96262-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="96262-120">See also</span></span>

- [<span data-ttu-id="96262-121">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="96262-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="96262-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="96262-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="96262-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="96262-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="96262-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="96262-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

