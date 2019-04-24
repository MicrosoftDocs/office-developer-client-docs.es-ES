---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328003"
---
# <a name="ftmuldw"></a><span data-ttu-id="5daa1-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="5daa1-103">FtMulDw</span></span>

  
  
<span data-ttu-id="5daa1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5daa1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5daa1-105">Multiplica un entero de 64 bits sin signo por un entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="5daa1-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5daa1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5daa1-106">Header file:</span></span>  <br/> |<span data-ttu-id="5daa1-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="5daa1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5daa1-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5daa1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5daa1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5daa1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5daa1-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5daa1-110">Called by:</span></span>  <br/> |<span data-ttu-id="5daa1-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="5daa1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="5daa1-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="5daa1-112">Parameters</span></span>

 <span data-ttu-id="5daa1-113">_Multiplicador_</span><span class="sxs-lookup"><span data-stu-id="5daa1-113">_Multiplier_</span></span>
  
> <span data-ttu-id="5daa1-114">a Una palabra doble que contiene el multiplicador de enteros de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="5daa1-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="5daa1-115">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="5daa1-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="5daa1-116">a Una estructura [FILETIME](filetime.md) que contiene el entero de 64 bits sin signo que se va a multiplicar por el valor en el parámetro _multiplicador_ .</span><span class="sxs-lookup"><span data-stu-id="5daa1-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5daa1-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5daa1-117">Return value</span></span>

<span data-ttu-id="5daa1-118">La función **FtMulDw** devuelve una estructura **FILETIME** que contiene el producto de los dos enteros.</span><span class="sxs-lookup"><span data-stu-id="5daa1-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="5daa1-119">Los dos parámetros de entrada permanecen sin cambios.</span><span class="sxs-lookup"><span data-stu-id="5daa1-119">The two input parameters remain unchanged.</span></span> 
  

