---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327275"
---
# <a name="fpropexists"></a><span data-ttu-id="d3612-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="d3612-103">FPropExists</span></span>

  
  
<span data-ttu-id="d3612-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3612-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3612-105">Busca una etiqueta de propiedad determinada en una interfaz [IMAPIProp](imapipropiunknown.md) o una interfaz derivada de **IMAPIProp**, como [IMessage](imessageimapiprop.md) o [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="d3612-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3612-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d3612-106">Header file:</span></span>  <br/> |<span data-ttu-id="d3612-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="d3612-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d3612-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d3612-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d3612-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d3612-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d3612-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d3612-110">Called by:</span></span>  <br/> |<span data-ttu-id="d3612-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d3612-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="d3612-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d3612-112">Parameters</span></span>

 <span data-ttu-id="d3612-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="d3612-113">_pobj_</span></span>
  
> <span data-ttu-id="d3612-114">a Puntero a la interfaz **IMAPIProp** o interfaz derivada de **IMAPIProp** en la que se va a buscar la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d3612-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="d3612-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="d3612-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="d3612-116">a Etiqueta de propiedad que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="d3612-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d3612-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3612-117">Return value</span></span>

<span data-ttu-id="d3612-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="d3612-118">TRUE</span></span> 
  
> <span data-ttu-id="d3612-119">Se encontró una coincidencia para la etiqueta de propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="d3612-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="d3612-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="d3612-120">FALSE</span></span> 
  
> <span data-ttu-id="d3612-121">No se encontró una coincidencia para la etiqueta de propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="d3612-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3612-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3612-122">Remarks</span></span>

<span data-ttu-id="d3612-123">Si la etiqueta de propiedad del parámetro _ulPropTag_ es de tipo PT_UNSPECIFIED, la función **FPropExists** busca una coincidencia basada solo en el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d3612-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="d3612-124">De lo contrario, la coincidencia es para toda la etiqueta de propiedad, incluido el tipo.</span><span class="sxs-lookup"><span data-stu-id="d3612-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

