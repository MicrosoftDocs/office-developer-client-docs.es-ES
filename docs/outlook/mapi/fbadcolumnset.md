---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b0260ffe5dc4806cb627fd71c78866bf96796455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434721"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="6a285-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="6a285-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="6a285-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a285-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a285-105">Comprueba la validez de un conjunto de columnas de tabla para su uso por parte de un proveedor de servicios en una llamada posterior al método [IMAPITable:: SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="6a285-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a285-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6a285-106">Header file:</span></span>  <br/> |<span data-ttu-id="6a285-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="6a285-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="6a285-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6a285-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6a285-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6a285-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6a285-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="6a285-110">Called by:</span></span>  <br/> |<span data-ttu-id="6a285-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="6a285-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="6a285-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a285-112">Parameters</span></span>

 <span data-ttu-id="6a285-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="6a285-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="6a285-114">a Puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedades que define las columnas de tabla que se deben validar.</span><span class="sxs-lookup"><span data-stu-id="6a285-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6a285-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a285-115">Return value</span></span>

<span data-ttu-id="6a285-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="6a285-116">TRUE</span></span> 
  
> <span data-ttu-id="6a285-117">El conjunto de columnas especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="6a285-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="6a285-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="6a285-118">FALSE</span></span> 
  
> <span data-ttu-id="6a285-119">El conjunto de columnas especificado es válido.</span><span class="sxs-lookup"><span data-stu-id="6a285-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a285-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6a285-120">Remarks</span></span>

<span data-ttu-id="6a285-121">La función **FBadColumnSet** trata las columnas de tipo PT_ERROR como no válidas y las columnas de tipo PT_NULL como válidas.</span><span class="sxs-lookup"><span data-stu-id="6a285-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

