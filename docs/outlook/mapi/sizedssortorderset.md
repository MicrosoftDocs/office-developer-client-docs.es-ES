---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2eb92c3f1555407a77332bd6ec3b2b7202f0553f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820699"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="73cc0-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="73cc0-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="73cc0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73cc0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73cc0-105">Crea una estructura de [SSortOrderSet](ssortorderset.md) con nombre que contiene un número especificado de criterios de ordenación.</span><span class="sxs-lookup"><span data-stu-id="73cc0-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73cc0-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="73cc0-106">Header file:</span></span>  <br/> |<span data-ttu-id="73cc0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73cc0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="73cc0-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="73cc0-108">Related structure:</span></span>  <br/> |<span data-ttu-id="73cc0-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="73cc0-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="73cc0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73cc0-110">Parameters</span></span>

<span data-ttu-id="73cc0-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="73cc0-111">__csort_</span></span>
  
> <span data-ttu-id="73cc0-112">Recuento de criterios de ordenación que se deben incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="73cc0-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="73cc0-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="73cc0-113">__name_</span></span>
  
> <span data-ttu-id="73cc0-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="73cc0-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73cc0-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73cc0-115">Remarks</span></span>

<span data-ttu-id="73cc0-116">Use la macro **SizedSSortOrderSet** para crear un criterio de ordenación establecer con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="73cc0-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="73cc0-117">Para usar la nueva estructura que el resultado de la macro **SizedSSortOrderSet** como un puntero a una estructura **SSortOrderSet** , realice la conversión de tipos siguiente:</span><span class="sxs-lookup"><span data-stu-id="73cc0-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="73cc0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="73cc0-118">See also</span></span>

- [<span data-ttu-id="73cc0-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="73cc0-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="73cc0-120">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="73cc0-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

