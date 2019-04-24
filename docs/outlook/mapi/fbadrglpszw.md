---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341058"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="3fb59-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="3fb59-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="3fb59-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fb59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fb59-105">Valida todas las cadenas de una matriz de cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="3fb59-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3fb59-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3fb59-106">Header file:</span></span>  <br/> |<span data-ttu-id="3fb59-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="3fb59-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="3fb59-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="3fb59-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3fb59-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3fb59-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3fb59-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="3fb59-110">Called by:</span></span>  <br/> |<span data-ttu-id="3fb59-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="3fb59-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="3fb59-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fb59-112">Parameters</span></span>

 <span data-ttu-id="3fb59-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="3fb59-113">_lppszW_</span></span>
  
> <span data-ttu-id="3fb59-114">a Puntero a una matriz de cadenas Unicode terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="3fb59-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="3fb59-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="3fb59-115">_cStrings_</span></span>
  
> <span data-ttu-id="3fb59-116">a Número de cadenas en la matriz a las que apunta el parámetro _lppszW_ .</span><span class="sxs-lookup"><span data-stu-id="3fb59-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3fb59-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fb59-117">Return value</span></span>

<span data-ttu-id="3fb59-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="3fb59-118">TRUE</span></span> 
  
> <span data-ttu-id="3fb59-119">Una o varias de las cadenas de la matriz especificada no son válidas.</span><span class="sxs-lookup"><span data-stu-id="3fb59-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="3fb59-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="3fb59-120">FALSE</span></span> 
  
> <span data-ttu-id="3fb59-121">Las cadenas de la matriz especificada son válidas.</span><span class="sxs-lookup"><span data-stu-id="3fb59-121">The strings in the specified array are valid.</span></span>
    

