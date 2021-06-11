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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410934"
---
# <a name="sizedsrowset"></a><span data-ttu-id="0eb2e-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="0eb2e-103">SizedSRowSet</span></span>

<span data-ttu-id="0eb2e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0eb2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0eb2e-105">Crea una estructura [SRowSet con](srowset.md) nombre que contiene un número especificado de filas.</span><span class="sxs-lookup"><span data-stu-id="0eb2e-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0eb2e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0eb2e-106">Header file:</span></span>  <br/> |<span data-ttu-id="0eb2e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0eb2e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0eb2e-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="0eb2e-108">Related structure:</span></span>  <br/> |<span data-ttu-id="0eb2e-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="0eb2e-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="0eb2e-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="0eb2e-110">Parameters</span></span>

<span data-ttu-id="0eb2e-111">_ _crow_</span><span class="sxs-lookup"><span data-stu-id="0eb2e-111">_ _crow_</span></span>
  
> <span data-ttu-id="0eb2e-112">Recuento del número de filas que se incluirán en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="0eb2e-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="0eb2e-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="0eb2e-113">_ _name_</span></span>
  
> <span data-ttu-id="0eb2e-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="0eb2e-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0eb2e-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0eb2e-115">Remarks</span></span>

<span data-ttu-id="0eb2e-116">Para usar la nueva estructura que resulta de la macro **SizedSRowSet** como puntero a una estructura **SRowSet,** realice la conversión siguiente:</span><span class="sxs-lookup"><span data-stu-id="0eb2e-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="0eb2e-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="0eb2e-117">See also</span></span>

- [<span data-ttu-id="0eb2e-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="0eb2e-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="0eb2e-119">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="0eb2e-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

