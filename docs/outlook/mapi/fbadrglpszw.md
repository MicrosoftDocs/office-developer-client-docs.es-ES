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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436443"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="9e1ae-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="9e1ae-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="9e1ae-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e1ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e1ae-105">Valida todas las cadenas de una matriz de cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="9e1ae-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e1ae-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9e1ae-106">Header file:</span></span>  <br/> |<span data-ttu-id="9e1ae-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="9e1ae-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="9e1ae-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9e1ae-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9e1ae-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9e1ae-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9e1ae-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9e1ae-110">Called by:</span></span>  <br/> |<span data-ttu-id="9e1ae-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="9e1ae-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="9e1ae-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e1ae-112">Parameters</span></span>

 <span data-ttu-id="9e1ae-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="9e1ae-113">_lppszW_</span></span>
  
> <span data-ttu-id="9e1ae-114">[entrada] Puntero a una matriz de cadenas Unicode terminadas en null.</span><span class="sxs-lookup"><span data-stu-id="9e1ae-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="9e1ae-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="9e1ae-115">_cStrings_</span></span>
  
> <span data-ttu-id="9e1ae-116">[entrada] Número de cadenas de la matriz a las que apunta el _parámetro lppszW._</span><span class="sxs-lookup"><span data-stu-id="9e1ae-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9e1ae-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e1ae-117">Return value</span></span>

<span data-ttu-id="9e1ae-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="9e1ae-118">TRUE</span></span> 
  
> <span data-ttu-id="9e1ae-119">Una o varias de las cadenas de la matriz especificada no son válidas.</span><span class="sxs-lookup"><span data-stu-id="9e1ae-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="9e1ae-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="9e1ae-120">FALSE</span></span> 
  
> <span data-ttu-id="9e1ae-121">Las cadenas de la matriz especificada son válidas.</span><span class="sxs-lookup"><span data-stu-id="9e1ae-121">The strings in the specified array are valid.</span></span>
    

