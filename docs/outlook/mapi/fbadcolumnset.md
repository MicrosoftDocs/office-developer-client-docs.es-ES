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
ms.openlocfilehash: 4e5f19258fb7716e741928f02a0a87f3939c74e0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575101"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="7919a-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="7919a-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="7919a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7919a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7919a-105">Las pruebas de la validez de una columna de tabla establecida para usar un proveedor de servicios en una llamada posterior al método [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="7919a-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7919a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7919a-106">Header file:</span></span>  <br/> |<span data-ttu-id="7919a-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="7919a-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="7919a-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="7919a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7919a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7919a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7919a-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7919a-110">Called by:</span></span>  <br/> |<span data-ttu-id="7919a-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="7919a-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="7919a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7919a-112">Parameters</span></span>

 <span data-ttu-id="7919a-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="7919a-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="7919a-114">[entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de definición de las columnas de tabla para validar las etiquetas (propiedad).</span><span class="sxs-lookup"><span data-stu-id="7919a-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7919a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7919a-115">Return value</span></span>

<span data-ttu-id="7919a-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="7919a-116">TRUE</span></span> 
  
> <span data-ttu-id="7919a-117">El conjunto de la columna especificada no es válido.</span><span class="sxs-lookup"><span data-stu-id="7919a-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="7919a-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="7919a-118">FALSE</span></span> 
  
> <span data-ttu-id="7919a-119">El conjunto de columnas especificado es válido.</span><span class="sxs-lookup"><span data-stu-id="7919a-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7919a-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7919a-120">Remarks</span></span>

<span data-ttu-id="7919a-121">La función **FBadColumnSet** trata a las columnas de tipo PT_ERROR como no válida y las columnas de tipo PT_NULL como válido.</span><span class="sxs-lookup"><span data-stu-id="7919a-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

