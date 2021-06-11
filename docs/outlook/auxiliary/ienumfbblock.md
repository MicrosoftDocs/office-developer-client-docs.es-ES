---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317629"
---
# <a name="ienumfbblock"></a><span data-ttu-id="b2d16-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="b2d16-102">IEnumFBBlock</span></span>

<span data-ttu-id="b2d16-103">Admite el acceso y la enumeración de bloques de datos de disponibilidad para un usuario dentro de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b2d16-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b2d16-104">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b2d16-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2d16-105">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="b2d16-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="b2d16-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2d16-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b2d16-107">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="b2d16-107">Provided by:</span></span>  <br/> |<span data-ttu-id="b2d16-108">Proveedor de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="b2d16-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="b2d16-109">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="b2d16-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b2d16-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="b2d16-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b2d16-111">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="b2d16-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b2d16-112">Next</span><span class="sxs-lookup"><span data-stu-id="b2d16-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="b2d16-113">Obtiene el siguiente número especificado de bloques de datos de disponibilidad en una enumeración.</span><span class="sxs-lookup"><span data-stu-id="b2d16-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="b2d16-114">Skip</span><span class="sxs-lookup"><span data-stu-id="b2d16-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="b2d16-115">Omite un número especificado de bloques de datos de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="b2d16-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="b2d16-116">Reset</span><span class="sxs-lookup"><span data-stu-id="b2d16-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="b2d16-117">Restablece el enumerador estableciendo el cursor en el principio.</span><span class="sxs-lookup"><span data-stu-id="b2d16-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="b2d16-118">Clone</span><span class="sxs-lookup"><span data-stu-id="b2d16-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="b2d16-119">Crea una copia del enumerador, con la misma restricción de tiempo pero estableciendo el cursor al principio del enumerador.</span><span class="sxs-lookup"><span data-stu-id="b2d16-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="b2d16-120">Restrict</span><span class="sxs-lookup"><span data-stu-id="b2d16-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="b2d16-121">Restringe la enumeración a un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="b2d16-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2d16-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2d16-122">Remarks</span></span>

<span data-ttu-id="b2d16-123">Una enumeración contiene bloques de datos de disponibilidad que no se superponen en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="b2d16-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="b2d16-124">Cuando hay elementos superpuestos en un calendario, Outlook combina estos elementos para formar bloques de disponibilidad no superpuestos en la enumeración en función de este orden de prioridad: fuera de la oficina, ocupado, provisional.</span><span class="sxs-lookup"><span data-stu-id="b2d16-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="b2d16-125">Un proveedor de disponibilidad obtiene esta interfaz y la enumeración de un intervalo de tiempo para un usuario a través [de IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="b2d16-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b2d16-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2d16-126">See also</span></span>

- [<span data-ttu-id="b2d16-127">Información sobre la API de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="b2d16-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="b2d16-128">Constantes (API de disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="b2d16-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="b2d16-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="b2d16-129">IFreeBusyData</span></span>](ifreebusydata.md)

