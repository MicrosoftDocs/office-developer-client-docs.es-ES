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
ms.openlocfilehash: 3f04c5be240f63d35ea8dba0f7abbf1085f2a41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816788"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="2eff4-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="2eff4-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="2eff4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2eff4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2eff4-105">Valida una matriz de estructuras que describen las propiedades con nombre y comprueba su asignación.</span><span class="sxs-lookup"><span data-stu-id="2eff4-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2eff4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2eff4-106">Header file:</span></span>  <br/> |<span data-ttu-id="2eff4-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="2eff4-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="2eff4-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="2eff4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2eff4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2eff4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2eff4-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="2eff4-110">Called by:</span></span>  <br/> |<span data-ttu-id="2eff4-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="2eff4-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="2eff4-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2eff4-112">Parameters</span></span>

 <span data-ttu-id="2eff4-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="2eff4-113">_lppNameId_</span></span>
  
> <span data-ttu-id="2eff4-114">[entrada] Puntero a una matriz de estructuras [MAPINAMEID](mapinameid.md) que describen las propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="2eff4-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="2eff4-115">_CNAME_</span><span class="sxs-lookup"><span data-stu-id="2eff4-115">_cNames_</span></span>
  
> <span data-ttu-id="2eff4-116">[entrada] Recuento de las estructuras de la propiedad con nombre en la matriz indicada por el parámetro _lppNameId_ .</span><span class="sxs-lookup"><span data-stu-id="2eff4-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2eff4-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2eff4-117">Return value</span></span>

<span data-ttu-id="2eff4-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="2eff4-118">TRUE</span></span> 
  
> <span data-ttu-id="2eff4-119">Una o varias de las estructuras de nombre de propiedad especificado no son válido.</span><span class="sxs-lookup"><span data-stu-id="2eff4-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="2eff4-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="2eff4-120">FALSE</span></span> 
  
> <span data-ttu-id="2eff4-121">Las estructuras de nombre de propiedad especificado son válidas.</span><span class="sxs-lookup"><span data-stu-id="2eff4-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2eff4-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2eff4-122">Remarks</span></span>

<span data-ttu-id="2eff4-123">La función **FBadRglpNameID** se puede usar al configurar para una llamada a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) o [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="2eff4-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

