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
ms.openlocfilehash: 7622baaebf6918cf84c48e53291cf5ec2c0b1a4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572567"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="86b3e-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="86b3e-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="86b3e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86b3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86b3e-105">Crea una estructura de [SSortOrderSet](ssortorderset.md) con nombre que contiene un número especificado de criterios de ordenación.</span><span class="sxs-lookup"><span data-stu-id="86b3e-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86b3e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="86b3e-106">Header file:</span></span>  <br/> |<span data-ttu-id="86b3e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86b3e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="86b3e-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="86b3e-108">Related structure:</span></span>  <br/> |<span data-ttu-id="86b3e-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="86b3e-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="86b3e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86b3e-110">Parameters</span></span>

<span data-ttu-id="86b3e-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="86b3e-111">__csort_</span></span>
  
> <span data-ttu-id="86b3e-112">Recuento de criterios de ordenación que se deben incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="86b3e-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="86b3e-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="86b3e-113">__name_</span></span>
  
> <span data-ttu-id="86b3e-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="86b3e-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="86b3e-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86b3e-115">Remarks</span></span>

<span data-ttu-id="86b3e-116">Use la macro **SizedSSortOrderSet** para crear un criterio de ordenación establecer con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="86b3e-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="86b3e-117">Para usar la nueva estructura que el resultado de la macro **SizedSSortOrderSet** como un puntero a una estructura **SSortOrderSet** , realice la conversión de tipos siguiente:</span><span class="sxs-lookup"><span data-stu-id="86b3e-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="86b3e-118">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="86b3e-118">See also</span></span>

- [<span data-ttu-id="86b3e-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="86b3e-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="86b3e-120">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="86b3e-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

