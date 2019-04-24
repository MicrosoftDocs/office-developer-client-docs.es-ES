---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Obtiene un intervalo de tiempo preestablecido para una enumeración de bloques de disponibilidad de datos para un usuario.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317531"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="c9f6e-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="c9f6e-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="c9f6e-104">Obtiene un intervalo de tiempo preestablecido para una enumeración de bloques de disponibilidad de datos para un usuario.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c9f6e-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c9f6e-105">Quick info</span></span>

<span data-ttu-id="c9f6e-106">Consulte [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="c9f6e-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="c9f6e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="c9f6e-107">Parameters</span></span>

<span data-ttu-id="c9f6e-108">_prtmStart_</span><span class="sxs-lookup"><span data-stu-id="c9f6e-108">_prtmStart_</span></span>
  
> <span data-ttu-id="c9f6e-109">contempla Un valor de tiempo relativo para el inicio de la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="c9f6e-110">Este valor es el número de minutos transcurridos desde el 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="c9f6e-111">_prtmEnd_</span><span class="sxs-lookup"><span data-stu-id="c9f6e-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="c9f6e-112">contempla Un valor de tiempo relativo para el fin de la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="c9f6e-113">Este valor es el número de minutos transcurridos desde el 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="c9f6e-114">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="c9f6e-114">Return values</span></span>

<span data-ttu-id="c9f6e-115">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c9f6e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9f6e-116">Remarks</span></span>

<span data-ttu-id="c9f6e-117">Un proveedor de disponibilidad llama a [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) o [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) para establecer el intervalo de tiempo de una enumeración.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="c9f6e-118">Si no se ha llamado a [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) o [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) , los valores predeterminados para **prtmStart** y **prtmEnd** deben estar establecidos entre el 1 de abril de 1601 00:00:00Z y el 31 de agosto de 4500 11:59:59Z poco.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="c9f6e-119">Además, no debe establecer la hora de inicio para que sea mayor que la hora de finalización.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="c9f6e-120">**IFreeBusyData:: GetFBPublishRange** debe devolver los valores almacenados en caché para el intervalo de tiempo establecido por la llamada más reciente para **IFreeBusyData:: EnumBlocks** o **IFreeBusyData:: SetFBRange**.</span><span class="sxs-lookup"><span data-stu-id="c9f6e-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c9f6e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9f6e-121">See also</span></span>

- [<span data-ttu-id="c9f6e-122">Utilizar un tiempo relativo a los datos de disponibilidad de acceso</span><span class="sxs-lookup"><span data-stu-id="c9f6e-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="c9f6e-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="c9f6e-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="c9f6e-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="c9f6e-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)

