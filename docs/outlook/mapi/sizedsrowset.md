---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282645"
---
# <a name="sizedsrowset"></a><span data-ttu-id="7cc7e-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="7cc7e-103">SizedSRowSet</span></span>

<span data-ttu-id="7cc7e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cc7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cc7e-105">Crea una estructura [SRowSet](srowset.md) con nombre que contiene un número especificado de filas.</span><span class="sxs-lookup"><span data-stu-id="7cc7e-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7cc7e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7cc7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="7cc7e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7cc7e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7cc7e-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="7cc7e-108">Related structure:</span></span>  <br/> |<span data-ttu-id="7cc7e-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="7cc7e-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="7cc7e-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="7cc7e-110">Parameters</span></span>

<span data-ttu-id="7cc7e-111">__patas_</span><span class="sxs-lookup"><span data-stu-id="7cc7e-111">__crow_</span></span>
  
> <span data-ttu-id="7cc7e-112">Número de filas que se van a incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="7cc7e-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="7cc7e-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="7cc7e-113">__name_</span></span>
  
> <span data-ttu-id="7cc7e-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="7cc7e-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7cc7e-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7cc7e-115">Remarks</span></span>

<span data-ttu-id="7cc7e-116">Para usar la nueva estructura que resulta de la macro **SizedSRowSet** como un puntero a una estructura **SRowSet** , realice la siguiente conversión:</span><span class="sxs-lookup"><span data-stu-id="7cc7e-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="7cc7e-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cc7e-117">See also</span></span>

- [<span data-ttu-id="7cc7e-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="7cc7e-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="7cc7e-119">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="7cc7e-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

