---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8f71b30bd02af8f768da86218456feadda8ea1b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414805"
---
# <a name="fequalnames"></a><span data-ttu-id="99b79-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="99b79-103">FEqualNames</span></span>

  
  
<span data-ttu-id="99b79-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99b79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99b79-105">Determina si dos propiedades con nombre MAPI son las mismas.</span><span class="sxs-lookup"><span data-stu-id="99b79-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99b79-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="99b79-106">Header file:</span></span>  <br/> |<span data-ttu-id="99b79-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="99b79-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="99b79-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="99b79-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="99b79-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="99b79-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="99b79-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="99b79-110">Called by:</span></span>  <br/> |<span data-ttu-id="99b79-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="99b79-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="99b79-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="99b79-112">Parameters</span></span>

 <span data-ttu-id="99b79-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="99b79-113">_lpName1_</span></span>
  
> <span data-ttu-id="99b79-114">[in] Puntero a una [estructura MAPINAMEID](mapinameid.md) que describe la primera propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="99b79-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="99b79-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="99b79-115">_lpName2_</span></span>
  
> <span data-ttu-id="99b79-116">[in] Puntero a una **estructura MAPINAMEID** que describe la segunda propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="99b79-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="99b79-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99b79-117">Return value</span></span>

<span data-ttu-id="99b79-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="99b79-118">TRUE</span></span> 
  
> <span data-ttu-id="99b79-119">Los dos nombres de propiedad son iguales.</span><span class="sxs-lookup"><span data-stu-id="99b79-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="99b79-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="99b79-120">FALSE</span></span> 
  
> <span data-ttu-id="99b79-121">Los dos nombres de propiedad no son iguales.</span><span class="sxs-lookup"><span data-stu-id="99b79-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99b79-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99b79-122">Remarks</span></span>

<span data-ttu-id="99b79-123">La **función FEqualNames** es útil porque la estructura **MAPINAMEID** contiene un [GUID](guid.md) y puede representar el propio nombre de la propiedad de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="99b79-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="99b79-124">Esto significa que los métodos binarios simples no pueden comparar las dos estructuras.</span><span class="sxs-lookup"><span data-stu-id="99b79-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="99b79-125">El proceso de prueba distingue mayúsculas de minúsculas para las cadenas de nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="99b79-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

