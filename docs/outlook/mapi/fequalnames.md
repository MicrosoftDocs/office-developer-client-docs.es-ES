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
ms.openlocfilehash: 0d8d1b8509f699b20f6e436d8af2c1d0d97cf4ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816802"
---
# <a name="fequalnames"></a><span data-ttu-id="ff4fe-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="ff4fe-103">FEqualNames</span></span>

  
  
<span data-ttu-id="ff4fe-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff4fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff4fe-105">Determina si dos MAPI con nombre de las propiedades son los mismos.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff4fe-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ff4fe-106">Header file:</span></span>  <br/> |<span data-ttu-id="ff4fe-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ff4fe-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ff4fe-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="ff4fe-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff4fe-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ff4fe-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ff4fe-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ff4fe-110">Called by:</span></span>  <br/> |<span data-ttu-id="ff4fe-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="ff4fe-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="ff4fe-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff4fe-112">Parameters</span></span>

 <span data-ttu-id="ff4fe-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="ff4fe-113">_lpName1_</span></span>
  
> <span data-ttu-id="ff4fe-114">[entrada] Puntero a una estructura [MAPINAMEID](mapinameid.md) que describe la primera propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="ff4fe-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="ff4fe-115">_lpName2_</span></span>
  
> <span data-ttu-id="ff4fe-116">[entrada] Puntero a una estructura **MAPINAMEID** que describe la segunda propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ff4fe-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff4fe-117">Return value</span></span>

<span data-ttu-id="ff4fe-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="ff4fe-118">TRUE</span></span> 
  
> <span data-ttu-id="ff4fe-119">Los nombres de dos propiedades son iguales.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="ff4fe-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="ff4fe-120">FALSE</span></span> 
  
> <span data-ttu-id="ff4fe-121">Los nombres de dos propiedades no son iguales.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff4fe-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ff4fe-122">Remarks</span></span>

<span data-ttu-id="ff4fe-123">La función **FEqualNames** es útil debido a que la estructura **MAPINAMEID** contiene un [GUID](guid.md) y puede representar el nombre de propiedad en más de una forma.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="ff4fe-124">Esto significa que no se pueden comparar las estructuras de dos métodos binario simple.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="ff4fe-125">El proceso de pruebas distingue mayúsculas de minúsculas para las cadenas de nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ff4fe-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

