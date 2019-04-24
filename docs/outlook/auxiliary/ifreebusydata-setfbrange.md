---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Establece el intervalo de tiempo para una enumeración de bloques de disponibilidad de datos para un usuario.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317482"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="cb2fc-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="cb2fc-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="cb2fc-104">Establece el intervalo de tiempo para una enumeración de bloques de disponibilidad de datos para un usuario.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cb2fc-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="cb2fc-105">Quick info</span></span>

<span data-ttu-id="cb2fc-106">Consulte [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="cb2fc-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="cb2fc-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="cb2fc-107">Parameters</span></span>

<span data-ttu-id="cb2fc-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="cb2fc-108">_rtmStart_</span></span>
  
> <span data-ttu-id="cb2fc-109">a Un valor de tiempo relativo para el inicio de la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="cb2fc-110">Este valor es el número de minutos transcurridos desde el 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="cb2fc-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="cb2fc-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="cb2fc-112">a Un valor de tiempo relativo para el fin de la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="cb2fc-113">Este valor es el número de minutos transcurridos desde el 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="cb2fc-114">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cb2fc-114">Return values</span></span>

<span data-ttu-id="cb2fc-115">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb2fc-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb2fc-116">Remarks</span></span>

<span data-ttu-id="cb2fc-117">Este método se usa para indicar el intervalo de tiempo de los elementos de calendario para los que se van a recuperar detalles.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="cb2fc-118">Los valores de *ftmStart* y *ftmEnd* se almacenan en caché y se devuelven en una llamada subsiguiente de [IFreeBusyData:: GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="cb2fc-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb2fc-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb2fc-119">See also</span></span>

- [<span data-ttu-id="cb2fc-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="cb2fc-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="cb2fc-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="cb2fc-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="cb2fc-122">Utilizar un tiempo relativo a los datos de disponibilidad de acceso</span><span class="sxs-lookup"><span data-stu-id="cb2fc-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

