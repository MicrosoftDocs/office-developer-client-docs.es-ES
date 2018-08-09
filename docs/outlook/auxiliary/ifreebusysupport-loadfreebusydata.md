---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Devuelve, para cada usuario especificado, una interfaz para enumerar los bloques de libre/ocupado de datos dentro de un intervalo de tiempo.
ms.openlocfilehash: 9af5a40da9f0a831de7346b44cee9ca004c02300
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816094"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="3ebee-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="3ebee-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="3ebee-104">Devuelve, para cada usuario especificado, una interfaz para enumerar los bloques de libre/ocupado de datos dentro de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3ebee-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3ebee-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="3ebee-105">Quick info</span></span>

<span data-ttu-id="3ebee-106">Vea [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="3ebee-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="3ebee-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ebee-107">Parameters</span></span>

<span data-ttu-id="3ebee-108">_Cmáx_</span><span class="sxs-lookup"><span data-stu-id="3ebee-108">_cMax_</span></span>
  
> <span data-ttu-id="3ebee-109">[entrada] El número de interfaces de [IFreeBusyData](ifreebusydata.md) para devolver.</span><span class="sxs-lookup"><span data-stu-id="3ebee-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="3ebee-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="3ebee-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="3ebee-111">[entrada] La matriz de disponibilidad a los usuarios para recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="3ebee-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="3ebee-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="3ebee-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="3ebee-113">[entrada] [out] La matriz de interfaces de **IFreeBusyData** que corresponden a la matriz _rgfbuser_ de estructuras [FBUser](fbuser.md) .</span><span class="sxs-lookup"><span data-stu-id="3ebee-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="3ebee-114">Esta matriz de punteros es asignada por el autor de la llamada y libera el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3ebee-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="3ebee-115">Las interfaces real que señala se liberan cuando el autor de la llamada se realiza con ellos.</span><span class="sxs-lookup"><span data-stu-id="3ebee-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="3ebee-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="3ebee-116">_phrStatus_</span></span>
  
> <span data-ttu-id="3ebee-117">[out] La matriz de resultados **HRESULT** para recuperar cada interfaz **IFreeBusyData** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="3ebee-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="3ebee-118">El valor puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="3ebee-118">The value may be NULL.</span></span> <span data-ttu-id="3ebee-119">Un resultado se establece en S_OK si correspondiente _prgfbdata_ es válida.</span><span class="sxs-lookup"><span data-stu-id="3ebee-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="3ebee-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="3ebee-120">_pcRead_</span></span>
  
>  <span data-ttu-id="3ebee-121">[out] El número real de los usuarios para el que se ha encontrado una interfaz **IFreeBusyData** .</span><span class="sxs-lookup"><span data-stu-id="3ebee-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="3ebee-122">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="3ebee-122">Return values</span></span>

<span data-ttu-id="3ebee-123">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="3ebee-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3ebee-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ebee-124">See also</span></span>

- [<span data-ttu-id="3ebee-125">Constantes (API de libre/ocupado)</span><span class="sxs-lookup"><span data-stu-id="3ebee-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

