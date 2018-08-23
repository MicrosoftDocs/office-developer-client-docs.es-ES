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
ms.openlocfilehash: 09c6540f2a224b7dc89a62c34cfb0c867cef4632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570852"
---
# <a name="fequalnames"></a><span data-ttu-id="54705-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="54705-103">FEqualNames</span></span>

  
  
<span data-ttu-id="54705-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54705-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54705-105">Determina si dos MAPI con nombre de las propiedades son los mismos.</span><span class="sxs-lookup"><span data-stu-id="54705-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54705-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="54705-106">Header file:</span></span>  <br/> |<span data-ttu-id="54705-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="54705-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="54705-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="54705-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="54705-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="54705-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="54705-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="54705-110">Called by:</span></span>  <br/> |<span data-ttu-id="54705-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="54705-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="54705-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54705-112">Parameters</span></span>

 <span data-ttu-id="54705-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="54705-113">_lpName1_</span></span>
  
> <span data-ttu-id="54705-114">[entrada] Puntero a una estructura [MAPINAMEID](mapinameid.md) que describe la primera propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="54705-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="54705-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="54705-115">_lpName2_</span></span>
  
> <span data-ttu-id="54705-116">[entrada] Puntero a una estructura **MAPINAMEID** que describe la segunda propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="54705-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="54705-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54705-117">Return value</span></span>

<span data-ttu-id="54705-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="54705-118">TRUE</span></span> 
  
> <span data-ttu-id="54705-119">Los nombres de dos propiedades son iguales.</span><span class="sxs-lookup"><span data-stu-id="54705-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="54705-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="54705-120">FALSE</span></span> 
  
> <span data-ttu-id="54705-121">Los nombres de dos propiedades no son iguales.</span><span class="sxs-lookup"><span data-stu-id="54705-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54705-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54705-122">Remarks</span></span>

<span data-ttu-id="54705-123">La función **FEqualNames** es útil debido a que la estructura **MAPINAMEID** contiene un [GUID](guid.md) y puede representar el nombre de propiedad en más de una forma.</span><span class="sxs-lookup"><span data-stu-id="54705-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="54705-124">Esto significa que no se pueden comparar las estructuras de dos métodos binario simple.</span><span class="sxs-lookup"><span data-stu-id="54705-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="54705-125">El proceso de pruebas distingue mayúsculas de minúsculas para las cadenas de nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="54705-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

