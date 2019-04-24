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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319407"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="a17e8-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="a17e8-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="a17e8-104">Devuelve, para cada usuario especificado, una interfaz para enumerar los bloques de disponibilidad de datos dentro de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a17e8-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a17e8-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="a17e8-105">Quick info</span></span>

<span data-ttu-id="a17e8-106">Consulte [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="a17e8-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="a17e8-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="a17e8-107">Parameters</span></span>

<span data-ttu-id="a17e8-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="a17e8-108">_cMax_</span></span>
  
> <span data-ttu-id="a17e8-109">a Número de interfaces de [IFreeBusyData](ifreebusydata.md) que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="a17e8-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="a17e8-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="a17e8-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="a17e8-111">a La matriz de usuarios de disponibilidad para el que se recuperarán los datos.</span><span class="sxs-lookup"><span data-stu-id="a17e8-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="a17e8-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="a17e8-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="a17e8-113">a contempla Matriz de interfaces de **IFreeBusyData** que corresponden a la matriz _Rgfbuser_ de estructuras [FBUser](fbuser.md) .</span><span class="sxs-lookup"><span data-stu-id="a17e8-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="a17e8-114">Esta matriz de punteros la asigna el autor de la llamada y la libera el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a17e8-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="a17e8-115">Las interfaces reales que apuntan se sueltan cuando el autor de la llamada se hace con ellas.</span><span class="sxs-lookup"><span data-stu-id="a17e8-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="a17e8-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="a17e8-116">_phrStatus_</span></span>
  
> <span data-ttu-id="a17e8-117">contempla La matriz de **HRESULT** produce la recuperación de cada interfaz **IFreeBusyData** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a17e8-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="a17e8-118">El valor puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a17e8-118">The value may be NULL.</span></span> <span data-ttu-id="a17e8-119">Un resultado se establece en S_OK si la _prgfbdata_ correspondiente es válida.</span><span class="sxs-lookup"><span data-stu-id="a17e8-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="a17e8-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="a17e8-120">_pcRead_</span></span>
  
>  <span data-ttu-id="a17e8-121">contempla El número real de usuarios para los que se ha encontrado una interfaz **IFreeBusyData** .</span><span class="sxs-lookup"><span data-stu-id="a17e8-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a17e8-122">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a17e8-122">Return values</span></span>

<span data-ttu-id="a17e8-123">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="a17e8-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a17e8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a17e8-124">See also</span></span>

- [<span data-ttu-id="a17e8-125">Constantes (API de disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="a17e8-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

