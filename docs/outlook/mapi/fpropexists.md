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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429491"
---
# <a name="fpropexists"></a><span data-ttu-id="03af8-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="03af8-103">FPropExists</span></span>

  
  
<span data-ttu-id="03af8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03af8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03af8-105">Busca una etiqueta de propiedad determinada en una interfaz [IMAPIProp](imapipropiunknown.md) o una interfaz derivada de **IMAPIProp**, como [IMessage](imessageimapiprop.md) o [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="03af8-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03af8-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="03af8-106">Header file:</span></span>  <br/> |<span data-ttu-id="03af8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="03af8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="03af8-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="03af8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="03af8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="03af8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="03af8-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="03af8-110">Called by:</span></span>  <br/> |<span data-ttu-id="03af8-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="03af8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="03af8-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="03af8-112">Parameters</span></span>

 <span data-ttu-id="03af8-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="03af8-113">_pobj_</span></span>
  
> <span data-ttu-id="03af8-114">[in] Puntero a la interfaz o interfaz **IMAPIProp** derivada de **IMAPIProp** en la que se va a buscar la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="03af8-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="03af8-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="03af8-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="03af8-116">[in] Etiqueta de propiedad para la que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="03af8-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="03af8-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03af8-117">Return value</span></span>

<span data-ttu-id="03af8-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="03af8-118">TRUE</span></span> 
  
> <span data-ttu-id="03af8-119">Se encontró una coincidencia para la etiqueta de propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="03af8-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="03af8-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="03af8-120">FALSE</span></span> 
  
> <span data-ttu-id="03af8-121">No se encontró una coincidencia para la etiqueta de propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="03af8-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03af8-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="03af8-122">Remarks</span></span>

<span data-ttu-id="03af8-123">Si la etiqueta de propiedad del parámetro  _ulPropTag_ tiene el tipo PT_UNSPECIFIED, la función **FPropExists** busca una coincidencia basada únicamente en el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="03af8-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="03af8-124">De lo contrario, la coincidencia es para toda la etiqueta de propiedad, incluido el tipo.</span><span class="sxs-lookup"><span data-stu-id="03af8-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

