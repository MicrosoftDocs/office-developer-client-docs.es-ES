---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Obtiene una interfaz que enumera los bloques de disponibilidad de los datos de un usuario dentro de un intervalo de tiempo especificado.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317559"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="d2d73-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="d2d73-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="d2d73-104">Obtiene una interfaz que enumera los bloques de disponibilidad de los datos de un usuario dentro de un intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="d2d73-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d2d73-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="d2d73-105">Quick info</span></span>

<span data-ttu-id="d2d73-106">Consulte [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="d2d73-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="d2d73-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d2d73-107">Parameters</span></span>

<span data-ttu-id="d2d73-108">_ppenumfb_</span><span class="sxs-lookup"><span data-stu-id="d2d73-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="d2d73-109">contempla Una interfaz para enumerar los bloques de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="d2d73-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="d2d73-110">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="d2d73-110">_ftmStart_</span></span>
  
> <span data-ttu-id="d2d73-111">a Hora de inicio de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="d2d73-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="d2d73-112">Se expresa en [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span><span class="sxs-lookup"><span data-stu-id="d2d73-112">It is expressed in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="d2d73-113">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="d2d73-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="d2d73-114">a La hora de finalización de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="d2d73-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="d2d73-115">Se expresa en **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="d2d73-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d2d73-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d2d73-116">Return values</span></span>

<span data-ttu-id="d2d73-117">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="d2d73-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2d73-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2d73-118">Remarks</span></span>

<span data-ttu-id="d2d73-119">Este método se usa para indicar el intervalo de tiempo de los elementos de calendario para los que se van a recuperar detalles.</span><span class="sxs-lookup"><span data-stu-id="d2d73-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="d2d73-120">Los valores de *ftmStart* y *ftmEnd* se almacenan en caché y se devuelven en una llamada subsiguiente de [IFreeBusyData:: GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="d2d73-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="d2d73-121">Un proveedor de disponibilidad también puede usar posteriormente la interfaz devuelta [IEnumFBBlock](ienumfbblock.md) para obtener acceso a la enumeración.</span><span class="sxs-lookup"><span data-stu-id="d2d73-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2d73-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2d73-122">See also</span></span>

- [<span data-ttu-id="d2d73-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="d2d73-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="d2d73-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="d2d73-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="d2d73-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="d2d73-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="d2d73-126">Utilizar un tiempo relativo a los datos de disponibilidad de acceso</span><span class="sxs-lookup"><span data-stu-id="d2d73-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

