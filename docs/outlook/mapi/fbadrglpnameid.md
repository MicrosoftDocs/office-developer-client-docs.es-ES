---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341037"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="c486c-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="c486c-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="c486c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c486c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c486c-105">Valida una matriz de estructuras que describen las propiedades con nombre y comprueba su asignación.</span><span class="sxs-lookup"><span data-stu-id="c486c-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c486c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c486c-106">Header file:</span></span>  <br/> |<span data-ttu-id="c486c-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c486c-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c486c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c486c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c486c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c486c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c486c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c486c-110">Called by:</span></span>  <br/> |<span data-ttu-id="c486c-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="c486c-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="c486c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c486c-112">Parameters</span></span>

 <span data-ttu-id="c486c-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="c486c-113">_lppNameId_</span></span>
  
> <span data-ttu-id="c486c-114">a Puntero a una matriz de estructuras [MAPINAMEID](mapinameid.md) que describen las propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="c486c-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="c486c-115">_CNAME_</span><span class="sxs-lookup"><span data-stu-id="c486c-115">_cNames_</span></span>
  
> <span data-ttu-id="c486c-116">a Número de estructuras de propiedad con nombre en la matriz señalada por el parámetro _lppNameId_ .</span><span class="sxs-lookup"><span data-stu-id="c486c-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c486c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c486c-117">Return value</span></span>

<span data-ttu-id="c486c-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="c486c-118">TRUE</span></span> 
  
> <span data-ttu-id="c486c-119">Una o varias de las estructuras de nombres de propiedad especificadas no son válidas.</span><span class="sxs-lookup"><span data-stu-id="c486c-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="c486c-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="c486c-120">FALSE</span></span> 
  
> <span data-ttu-id="c486c-121">Las estructuras de nombres de propiedad especificadas son válidas.</span><span class="sxs-lookup"><span data-stu-id="c486c-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c486c-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c486c-122">Remarks</span></span>

<span data-ttu-id="c486c-123">La función **FBadRglpNameID** se puede usar al configurar una llamada a [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) o [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="c486c-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

