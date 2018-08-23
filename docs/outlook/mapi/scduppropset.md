---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8bbe8aa00ce446d228c23e1d474fa5140ae7b40a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581982"
---
# <a name="scduppropset"></a><span data-ttu-id="e7a92-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="e7a92-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="e7a92-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7a92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7a92-105">Duplica una matriz de valores de propiedad en un único bloque de memoria MAPI combinar las operaciones de las funciones [ScCopyProps](sccopyprops.md) y [ScCountProps](sccountprops.md) .</span><span class="sxs-lookup"><span data-stu-id="e7a92-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7a92-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e7a92-106">Header file:</span></span>  <br/> |<span data-ttu-id="e7a92-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e7a92-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e7a92-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="e7a92-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7a92-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e7a92-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e7a92-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e7a92-110">Called by:</span></span>  <br/> |<span data-ttu-id="e7a92-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="e7a92-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="e7a92-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7a92-112">Parameters</span></span>

 <span data-ttu-id="e7a92-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="e7a92-113">_cprop_</span></span>
  
> <span data-ttu-id="e7a92-114">[entrada] Recuento de valores de propiedad en la matriz indicada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="e7a92-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="e7a92-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="e7a92-115">_rgprop_</span></span>
  
> <span data-ttu-id="e7a92-116">[entrada] Puntero a una matriz de estructuras [SPropValue](spropvalue.md) definición de los valores de propiedad que se va a duplicar.</span><span class="sxs-lookup"><span data-stu-id="e7a92-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="e7a92-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e7a92-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e7a92-118">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria para la matriz duplicada.</span><span class="sxs-lookup"><span data-stu-id="e7a92-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="e7a92-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="e7a92-119">_prgprop_</span></span>
  
> <span data-ttu-id="e7a92-120">[out] Puntero a la posición inicial en la memoria donde se almacena la matriz devuelta duplicada de estructuras **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="e7a92-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e7a92-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7a92-121">Return value</span></span>

<span data-ttu-id="e7a92-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7a92-122">S_OK</span></span> 
  
> <span data-ttu-id="e7a92-123">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="e7a92-123">The call succeeded and has returned the expected value or values.</span></span>
    

