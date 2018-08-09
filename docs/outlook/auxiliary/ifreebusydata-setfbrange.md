---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Establece el intervalo de tiempo para una enumeración de libre/ocupado de bloques de datos para un usuario.
ms.openlocfilehash: 84a25a2dd43f594caa075d90e4f183086452184a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816109"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="26588-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="26588-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="26588-104">Establece el intervalo de tiempo para una enumeración de libre/ocupado de bloques de datos para un usuario.</span><span class="sxs-lookup"><span data-stu-id="26588-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="26588-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="26588-105">Quick info</span></span>

<span data-ttu-id="26588-106">Vea [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="26588-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="26588-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26588-107">Parameters</span></span>

<span data-ttu-id="26588-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="26588-108">_rtmStart_</span></span>
  
> <span data-ttu-id="26588-109">[entrada] Un valor de tiempo relativo para el inicio de la información de libre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="26588-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="26588-110">Este valor es el número de minutos desde el 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="26588-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="26588-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="26588-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="26588-112">[entrada] Un valor de tiempo relativo para el final de la información de libre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="26588-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="26588-113">Este valor es el número de minutos desde el 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="26588-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="26588-114">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="26588-114">Return values</span></span>

<span data-ttu-id="26588-115">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="26588-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26588-116">Notas</span><span class="sxs-lookup"><span data-stu-id="26588-116">Remarks</span></span>

<span data-ttu-id="26588-117">Este método se usa para indicar el intervalo de tiempo de los elementos del calendario para el que se va a recuperar detalles.</span><span class="sxs-lookup"><span data-stu-id="26588-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="26588-118">Los valores de *ftmStart* y *ftmEnd* se almacena en caché y se devuelven en una llamada posterior de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="26588-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26588-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="26588-119">See also</span></span>

- [<span data-ttu-id="26588-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="26588-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="26588-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="26588-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="26588-122">Utilizar un tiempo relativo a los datos de disponibilidad de acceso</span><span class="sxs-lookup"><span data-stu-id="26588-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

