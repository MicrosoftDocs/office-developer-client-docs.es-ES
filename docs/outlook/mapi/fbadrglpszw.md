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
ms.openlocfilehash: 3b3b6b5ca0b06fc55a60e035ffd9118391cab8f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565917"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="7a934-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="7a934-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="7a934-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a934-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a934-105">Valida todas las cadenas de una matriz de cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="7a934-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a934-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7a934-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a934-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="7a934-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="7a934-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="7a934-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7a934-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7a934-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7a934-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7a934-110">Called by:</span></span>  <br/> |<span data-ttu-id="7a934-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="7a934-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="7a934-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a934-112">Parameters</span></span>

 <span data-ttu-id="7a934-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="7a934-113">_lppszW_</span></span>
  
> <span data-ttu-id="7a934-114">[entrada] Puntero a una matriz de cadenas de Unicode terminada en null.</span><span class="sxs-lookup"><span data-stu-id="7a934-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="7a934-115">_objetos CString_</span><span class="sxs-lookup"><span data-stu-id="7a934-115">_cStrings_</span></span>
  
> <span data-ttu-id="7a934-116">[entrada] Recuento de las cadenas en la matriz indicada por el parámetro _lppszW_ .</span><span class="sxs-lookup"><span data-stu-id="7a934-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7a934-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a934-117">Return value</span></span>

<span data-ttu-id="7a934-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="7a934-118">TRUE</span></span> 
  
> <span data-ttu-id="7a934-119">Una o varias de las cadenas de la matriz especificada no son válidos.</span><span class="sxs-lookup"><span data-stu-id="7a934-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="7a934-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="7a934-120">FALSE</span></span> 
  
> <span data-ttu-id="7a934-121">Las cadenas de la matriz especificada son válidas.</span><span class="sxs-lookup"><span data-stu-id="7a934-121">The strings in the specified array are valid.</span></span>
    

