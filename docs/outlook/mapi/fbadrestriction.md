---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 43e0d8d28836b3114ab2029bc1f241197c569ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816794"
---
# <a name="fbadrestriction"></a><span data-ttu-id="e60dd-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="e60dd-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="e60dd-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e60dd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e60dd-105">Valida una restricción que se usa para limitar una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="e60dd-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e60dd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e60dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="e60dd-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="e60dd-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="e60dd-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="e60dd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e60dd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e60dd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e60dd-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e60dd-110">Called by:</span></span>  <br/> |<span data-ttu-id="e60dd-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="e60dd-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="e60dd-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e60dd-112">Parameters</span></span>

 <span data-ttu-id="e60dd-113">_lpres_</span><span class="sxs-lookup"><span data-stu-id="e60dd-113">_lpres_</span></span>
  
> <span data-ttu-id="e60dd-114">[entrada] Una estructura [SRestriction](srestriction.md) definición de la restricción que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="e60dd-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e60dd-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e60dd-115">Return value</span></span>

<span data-ttu-id="e60dd-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="e60dd-116">TRUE</span></span> 
  
> <span data-ttu-id="e60dd-117">La restricción especificada, o una o varias de sus subrestrictions, no están válido.</span><span class="sxs-lookup"><span data-stu-id="e60dd-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="e60dd-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="e60dd-118">FALSE</span></span> 
  
> <span data-ttu-id="e60dd-119">La restricción especificada y todas sus subrestrictions son válidos.</span><span class="sxs-lookup"><span data-stu-id="e60dd-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e60dd-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e60dd-120">Remarks</span></span>

<span data-ttu-id="e60dd-121">Una vez que se valida una restricción, puede pasarse en llamadas al método [IMAPITable:: Restrict](imapitable-restrict.md) para restringir la tabla a algunas filas, al método [IMAPITable:: FindRow](imapitable-findrow.md) para localizar una fila de tabla y a los métodos de la [IMAPIContainer](imapicontainerimapiprop.md) interfaz para llevar a cabo una restricción en un objeto contenedor.</span><span class="sxs-lookup"><span data-stu-id="e60dd-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

