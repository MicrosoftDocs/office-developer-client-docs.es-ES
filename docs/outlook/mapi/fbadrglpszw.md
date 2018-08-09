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
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816790"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="f6059-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="f6059-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="f6059-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f6059-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f6059-105">Valida todas las cadenas de una matriz de cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="f6059-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6059-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f6059-106">Header file:</span></span>  <br/> |<span data-ttu-id="f6059-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f6059-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f6059-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="f6059-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f6059-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f6059-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f6059-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f6059-110">Called by:</span></span>  <br/> |<span data-ttu-id="f6059-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="f6059-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="f6059-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6059-112">Parameters</span></span>

 <span data-ttu-id="f6059-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="f6059-113">_lppszW_</span></span>
  
> <span data-ttu-id="f6059-114">[entrada] Puntero a una matriz de cadenas de Unicode terminada en null.</span><span class="sxs-lookup"><span data-stu-id="f6059-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="f6059-115">_objetos CString_</span><span class="sxs-lookup"><span data-stu-id="f6059-115">_cStrings_</span></span>
  
> <span data-ttu-id="f6059-116">[entrada] Recuento de las cadenas en la matriz indicada por el parámetro _lppszW_ .</span><span class="sxs-lookup"><span data-stu-id="f6059-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f6059-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6059-117">Return value</span></span>

<span data-ttu-id="f6059-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="f6059-118">TRUE</span></span> 
  
> <span data-ttu-id="f6059-119">Una o varias de las cadenas de la matriz especificada no son válidos.</span><span class="sxs-lookup"><span data-stu-id="f6059-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="f6059-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="f6059-120">FALSE</span></span> 
  
> <span data-ttu-id="f6059-121">Las cadenas de la matriz especificada son válidas.</span><span class="sxs-lookup"><span data-stu-id="f6059-121">The strings in the specified array are valid.</span></span>
    

