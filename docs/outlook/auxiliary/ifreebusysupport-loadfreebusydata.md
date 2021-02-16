---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Devuelve, para cada usuario especificado, una interfaz para enumerar bloques de datos de disponibilidad dentro de un intervalo de tiempo.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411235"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="af40e-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="af40e-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="af40e-104">Devuelve, para cada usuario especificado, una interfaz para enumerar bloques de datos de disponibilidad dentro de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="af40e-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="af40e-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="af40e-105">Quick info</span></span>

<span data-ttu-id="af40e-106">Vea [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="af40e-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="af40e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af40e-107">Parameters</span></span>

<span data-ttu-id="af40e-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="af40e-108">_cMax_</span></span>
  
> <span data-ttu-id="af40e-109">[entrada] Número de interfaces [IFreeBusyData](ifreebusydata.md) que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="af40e-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="af40e-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="af40e-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="af40e-111">[entrada] Matriz de usuarios de disponibilidad para los que recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="af40e-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="af40e-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="af40e-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="af40e-113">[entrada] [salida] Matriz de **interfaces IFreeBusyData** que corresponden a la matriz _rgfbuser_ de las [estructuras FBUser.](fbuser.md)</span><span class="sxs-lookup"><span data-stu-id="af40e-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="af40e-114">Esta matriz de punteros la asigna el autor de la llamada y la libera.</span><span class="sxs-lookup"><span data-stu-id="af40e-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="af40e-115">Las interfaces reales a las que apunta se liberan cuando el autor de la llamada ha terminado con ellas.</span><span class="sxs-lookup"><span data-stu-id="af40e-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="af40e-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="af40e-116">_phrStatus_</span></span>
  
> <span data-ttu-id="af40e-117">[salida] Matriz de **resultados HRESULT** para recuperar cada interfaz **IFreeBusyData** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="af40e-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="af40e-118">El valor puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="af40e-118">The value may be NULL.</span></span> <span data-ttu-id="af40e-119">Un resultado se establece en S_OK si el  _prgfbdata correspondiente_ es válido.</span><span class="sxs-lookup"><span data-stu-id="af40e-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="af40e-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="af40e-120">_pcRead_</span></span>
  
>  <span data-ttu-id="af40e-121">[salida] Número real de usuarios para los que se ha encontrado una **interfaz IFreeBusyData.**</span><span class="sxs-lookup"><span data-stu-id="af40e-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="af40e-122">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="af40e-122">Return values</span></span>

<span data-ttu-id="af40e-123">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="af40e-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af40e-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="af40e-124">See also</span></span>

- [<span data-ttu-id="af40e-125">Constantes (API de disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="af40e-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

