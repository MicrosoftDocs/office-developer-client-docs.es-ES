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
ms.openlocfilehash: b8c70c8b13025f196fdebb2956939bec840a96f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583942"
---
# <a name="sizedsrowset"></a><span data-ttu-id="930ea-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="930ea-103">SizedSRowSet</span></span>

<span data-ttu-id="930ea-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="930ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="930ea-105">Crea una estructura de [SRowSet](srowset.md) con nombre que contiene un número especificado de filas.</span><span class="sxs-lookup"><span data-stu-id="930ea-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="930ea-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="930ea-106">Header file:</span></span>  <br/> |<span data-ttu-id="930ea-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="930ea-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="930ea-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="930ea-108">Related structure:</span></span>  <br/> |<span data-ttu-id="930ea-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="930ea-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="930ea-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="930ea-110">Parameters</span></span>

<span data-ttu-id="930ea-111">__gallo_</span><span class="sxs-lookup"><span data-stu-id="930ea-111">__crow_</span></span>
  
> <span data-ttu-id="930ea-112">Recuento del número de filas que se deben incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="930ea-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="930ea-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="930ea-113">__name_</span></span>
  
> <span data-ttu-id="930ea-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="930ea-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="930ea-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="930ea-115">Remarks</span></span>

<span data-ttu-id="930ea-116">Para usar la nueva estructura que el resultado de la macro **SizedSRowSet** como un puntero a una estructura **SRowSet** , realice la conversión de tipos siguiente:</span><span class="sxs-lookup"><span data-stu-id="930ea-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="930ea-117">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="930ea-117">See also</span></span>

- [<span data-ttu-id="930ea-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="930ea-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="930ea-119">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="930ea-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

