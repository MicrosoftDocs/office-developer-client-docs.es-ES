---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9be25dc655536ff5d32a635da57c54ebd12fea0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816892"
---
# <a name="ftadcft"></a><span data-ttu-id="b342d-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="b342d-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="b342d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b342d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b342d-105">Agrega un entero de 64 bits sin signo a otro, de forma opcional mediante una marca de transporte.</span><span class="sxs-lookup"><span data-stu-id="b342d-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b342d-106">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="b342d-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="b342d-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="b342d-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="b342d-108">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b342d-108">Called by:</span></span>  <br/> |<span data-ttu-id="b342d-109">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="b342d-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="b342d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b342d-110">Parameters</span></span>

 <span data-ttu-id="b342d-111">_FT1_</span><span class="sxs-lookup"><span data-stu-id="b342d-111">_ft1_</span></span>
  
> <span data-ttu-id="b342d-112">[entrada] Una estructura [FILETIME](filetime.md) que contiene el primer entero de 64 bits sin signo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="b342d-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="b342d-113">_pies2_</span><span class="sxs-lookup"><span data-stu-id="b342d-113">_ft2_</span></span>
  
> <span data-ttu-id="b342d-114">[entrada] Una estructura FILETIME que contiene el segundo entero de 64 bits sin signo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="b342d-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="b342d-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="b342d-115">_pwCarry_</span></span>
  
> <span data-ttu-id="b342d-116">[entrada, salida, opcional] En la entrada, un puntero a la entrada de llevar a cabo marca.</span><span class="sxs-lookup"><span data-stu-id="b342d-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="b342d-117">En la salida, un puntero al resultado de la adición encontrará.</span><span class="sxs-lookup"><span data-stu-id="b342d-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="b342d-118">Este parámetro puede ser NULL si el resultado de transporte no es necesario.</span><span class="sxs-lookup"><span data-stu-id="b342d-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b342d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b342d-119">Return value</span></span>

<span data-ttu-id="b342d-120">La función **FtAdcFt** devuelve una estructura **FILETIME** que contiene la suma de los dos números enteros.</span><span class="sxs-lookup"><span data-stu-id="b342d-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="b342d-121">No se modifican los dos parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="b342d-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="b342d-122">Si **pwCarry** no es NULL, contiene el resultado de transporte para la suma, 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="b342d-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b342d-123">Notas</span><span class="sxs-lookup"><span data-stu-id="b342d-123">Remarks</span></span>

<span data-ttu-id="b342d-124">La función **FtAdcFt** es idéntica a **FtAddFt** cuando _pwCarry_ es NULL.</span><span class="sxs-lookup"><span data-stu-id="b342d-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="b342d-125">Si _pwCarry_ no es NULL y puntos en 0, **FtAdcFt** devuelve el mismo valor **FILETIME** que devuelve **FtAddFt** .</span><span class="sxs-lookup"><span data-stu-id="b342d-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b342d-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="b342d-126">See also</span></span>



[<span data-ttu-id="b342d-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="b342d-127">FtAddFt</span></span>](ftaddft.md)

