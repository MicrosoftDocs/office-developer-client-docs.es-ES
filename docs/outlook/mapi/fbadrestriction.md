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
ms.openlocfilehash: eb3e0d5a96121f63166da2025743b7ef89f4ecf6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340967"
---
# <a name="fbadrestriction"></a><span data-ttu-id="10000-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="10000-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="10000-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10000-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10000-105">Valida una restricción usada para limitar una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="10000-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10000-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="10000-106">Header file:</span></span>  <br/> |<span data-ttu-id="10000-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="10000-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="10000-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="10000-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="10000-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="10000-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="10000-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="10000-110">Called by:</span></span>  <br/> |<span data-ttu-id="10000-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="10000-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="10000-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10000-112">Parameters</span></span>

 <span data-ttu-id="10000-113">_lpres_</span><span class="sxs-lookup"><span data-stu-id="10000-113">_lpres_</span></span>
  
> <span data-ttu-id="10000-114">a Estructura [SRestriction](srestriction.md) que define la restricción que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="10000-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="10000-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10000-115">Return value</span></span>

<span data-ttu-id="10000-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="10000-116">TRUE</span></span> 
  
> <span data-ttu-id="10000-117">La restricción especificada o una o varias de sus subrestricciones no son válidas.</span><span class="sxs-lookup"><span data-stu-id="10000-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="10000-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="10000-118">FALSE</span></span> 
  
> <span data-ttu-id="10000-119">La restricción especificada y todas sus subrestricciones son válidas.</span><span class="sxs-lookup"><span data-stu-id="10000-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10000-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="10000-120">Remarks</span></span>

<span data-ttu-id="10000-121">Una vez validada la restricción, se puede pasar en llamadas al método [IMAPITable:: Restrict](imapitable-restrict.md) para restringir la tabla a determinadas filas, al método [IMAPITable:: FindRow](imapitable-findrow.md) para localizar una fila de tabla y a los métodos de [IMAPIContainer](imapicontainerimapiprop.md) interfaz para realizar una restricción en un objeto contenedor.</span><span class="sxs-lookup"><span data-stu-id="10000-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

