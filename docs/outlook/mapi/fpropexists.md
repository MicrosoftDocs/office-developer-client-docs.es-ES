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
ms.openlocfilehash: 0d016c83678d9c1c94ee4ad4b8e12723c03f7bda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570439"
---
# <a name="fpropexists"></a><span data-ttu-id="3f84c-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="3f84c-103">FPropExists</span></span>

  
  
<span data-ttu-id="3f84c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f84c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f84c-105">Busca una etiqueta de propiedad determinada en una interfaz [IMAPIProp](imapipropiunknown.md) o una interfaz derivada de **IMAPIProp**, como [IMessage](imessageimapiprop.md) o [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="3f84c-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f84c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3f84c-106">Header file:</span></span>  <br/> |<span data-ttu-id="3f84c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3f84c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3f84c-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="3f84c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3f84c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3f84c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3f84c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="3f84c-110">Called by:</span></span>  <br/> |<span data-ttu-id="3f84c-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="3f84c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="3f84c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f84c-112">Parameters</span></span>

 <span data-ttu-id="3f84c-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="3f84c-113">_pobj_</span></span>
  
> <span data-ttu-id="3f84c-114">[entrada] Puntero a la interfaz de **IMAPIProp** o interfaz derivada de **IMAPIProp** dentro de la que se va a buscar la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="3f84c-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="3f84c-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="3f84c-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="3f84c-116">[entrada] Etiqueta de la propiedad que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="3f84c-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3f84c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f84c-117">Return value</span></span>

<span data-ttu-id="3f84c-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="3f84c-118">TRUE</span></span> 
  
> <span data-ttu-id="3f84c-119">Se encontró una coincidencia para la etiqueta de la propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="3f84c-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="3f84c-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="3f84c-120">FALSE</span></span> 
  
> <span data-ttu-id="3f84c-121">No se encontró una coincidencia para la etiqueta de la propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="3f84c-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f84c-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f84c-122">Remarks</span></span>

<span data-ttu-id="3f84c-123">Si la etiqueta de propiedad en el parámetro _ulPropTag_ no tiene tipo PT_UNSPECIFIED, la función **FPropExists** busca una coincidencia basándose exclusivamente en el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3f84c-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="3f84c-124">De lo contrario, la coincidencia es para la etiqueta de propiedad completa, incluido el tipo.</span><span class="sxs-lookup"><span data-stu-id="3f84c-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

