---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Devuelve, para cada usuario especificado, una interfaz para enumerar los bloques de disponibilidad de datos dentro de un intervalo de tiempo.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411235"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="142da-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="142da-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="142da-104">Devuelve, para cada usuario especificado, una interfaz para enumerar los bloques de disponibilidad de datos dentro de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="142da-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="142da-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="142da-105">Quick info</span></span>

<span data-ttu-id="142da-106">Consulte [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="142da-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="142da-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="142da-107">Parameters</span></span>

<span data-ttu-id="142da-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="142da-108">_cMax_</span></span>
  
> <span data-ttu-id="142da-109">a Número de interfaces de [IFreeBusyData](ifreebusydata.md) que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="142da-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="142da-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="142da-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="142da-111">a La matriz de usuarios de disponibilidad para el que se recuperarán los datos.</span><span class="sxs-lookup"><span data-stu-id="142da-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="142da-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="142da-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="142da-113">a contempla Matriz de interfaces de **IFreeBusyData** que corresponden a la matriz _Rgfbuser_ de estructuras [FBUser](fbuser.md) .</span><span class="sxs-lookup"><span data-stu-id="142da-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="142da-114">Esta matriz de punteros la asigna el autor de la llamada y la libera el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="142da-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="142da-115">Las interfaces reales que apuntan se sueltan cuando el autor de la llamada se hace con ellas.</span><span class="sxs-lookup"><span data-stu-id="142da-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="142da-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="142da-116">_phrStatus_</span></span>
  
> <span data-ttu-id="142da-117">contempla La matriz de **HRESULT** produce la recuperación de cada interfaz **IFreeBusyData** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="142da-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="142da-118">El valor puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="142da-118">The value may be NULL.</span></span> <span data-ttu-id="142da-119">Un resultado se establece en S_OK si la _prgfbdata_ correspondiente es válida.</span><span class="sxs-lookup"><span data-stu-id="142da-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="142da-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="142da-120">_pcRead_</span></span>
  
>  <span data-ttu-id="142da-121">contempla El número real de usuarios para los que se ha encontrado una interfaz **IFreeBusyData** .</span><span class="sxs-lookup"><span data-stu-id="142da-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="142da-122">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="142da-122">Return values</span></span>

<span data-ttu-id="142da-123">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="142da-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="142da-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="142da-124">See also</span></span>

- [<span data-ttu-id="142da-125">Constantes (API de disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="142da-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

