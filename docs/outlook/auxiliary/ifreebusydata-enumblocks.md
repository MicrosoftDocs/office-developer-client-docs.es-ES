---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Obtiene una interfaz que se enumera los bloques de disponibilidad de datos para un usuario dentro de un intervalo de tiempo especificado.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394541"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="b5332-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="b5332-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="b5332-104">Obtiene una interfaz que se enumera los bloques de disponibilidad de datos para un usuario dentro de un intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="b5332-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b5332-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b5332-105">Quick info</span></span>

<span data-ttu-id="b5332-106">Vea [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="b5332-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="b5332-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5332-107">Parameters</span></span>

<span data-ttu-id="b5332-108">_ppenumfb_</span><span class="sxs-lookup"><span data-stu-id="b5332-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="b5332-109">[out] Una interfaz para enumerar los bloques de libre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="b5332-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="b5332-110">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="b5332-110">_ftmStart_</span></span>
  
> <span data-ttu-id="b5332-111">[entrada] La hora de inicio para la enumeración.</span><span class="sxs-lookup"><span data-stu-id="b5332-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="b5332-112">Se expresa en [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span><span class="sxs-lookup"><span data-stu-id="b5332-112">It is expressed in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="b5332-113">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="b5332-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="b5332-114">[entrada] La hora de finalización para la enumeración.</span><span class="sxs-lookup"><span data-stu-id="b5332-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="b5332-115">Se expresa en **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="b5332-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b5332-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b5332-116">Return values</span></span>

<span data-ttu-id="b5332-117">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b5332-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5332-118">Notas</span><span class="sxs-lookup"><span data-stu-id="b5332-118">Remarks</span></span>

<span data-ttu-id="b5332-119">Este método se usa para indicar el intervalo de tiempo de los elementos del calendario para el que se va a recuperar detalles.</span><span class="sxs-lookup"><span data-stu-id="b5332-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="b5332-120">Los valores de *ftmStart* y *ftmEnd* se almacena en caché y se devuelven en una llamada posterior de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="b5332-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="b5332-121">Un proveedor de libre/ocupado posteriormente también puede usar la interfaz de [IEnumFBBlock](ienumfbblock.md) devuelta para tener acceso a la enumeración.</span><span class="sxs-lookup"><span data-stu-id="b5332-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b5332-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5332-122">See also</span></span>

- [<span data-ttu-id="b5332-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="b5332-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="b5332-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="b5332-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="b5332-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="b5332-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="b5332-126">Utilizar un tiempo relativo a los datos de disponibilidad de acceso</span><span class="sxs-lookup"><span data-stu-id="b5332-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

