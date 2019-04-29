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
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428609"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="dab3b-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="dab3b-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="dab3b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dab3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dab3b-105">Crea una estructura [SSortOrderSet](ssortorderset.md) con nombre que contiene un número especificado de criterios de ordenación.</span><span class="sxs-lookup"><span data-stu-id="dab3b-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dab3b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="dab3b-106">Header file:</span></span>  <br/> |<span data-ttu-id="dab3b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dab3b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dab3b-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="dab3b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="dab3b-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="dab3b-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="dab3b-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="dab3b-110">Parameters</span></span>

<span data-ttu-id="dab3b-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="dab3b-111">__csort_</span></span>
  
> <span data-ttu-id="dab3b-112">Número de criterios de ordenación que se van a incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="dab3b-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="dab3b-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="dab3b-113">__name_</span></span>
  
> <span data-ttu-id="dab3b-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="dab3b-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dab3b-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dab3b-115">Remarks</span></span>

<span data-ttu-id="dab3b-116">Use la macro **SizedSSortOrderSet** para crear un conjunto de orden con los límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="dab3b-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="dab3b-117">Para usar la nueva estructura que resulta de la macro **SizedSSortOrderSet** como un puntero a una estructura **SSortOrderSet** , realice la siguiente conversión:</span><span class="sxs-lookup"><span data-stu-id="dab3b-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="dab3b-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="dab3b-118">See also</span></span>

- [<span data-ttu-id="dab3b-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="dab3b-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="dab3b-120">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="dab3b-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

