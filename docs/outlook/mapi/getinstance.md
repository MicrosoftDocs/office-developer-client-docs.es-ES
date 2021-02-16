---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418725"
---
# <a name="getinstance"></a><span data-ttu-id="92e5b-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="92e5b-103">GetInstance</span></span>

  
  
<span data-ttu-id="92e5b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92e5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92e5b-105">Copia un valor dentro de una propiedad multivalor en una propiedad de un solo valor del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="92e5b-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92e5b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="92e5b-106">Header file:</span></span>  <br/> |<span data-ttu-id="92e5b-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="92e5b-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="92e5b-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="92e5b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="92e5b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="92e5b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="92e5b-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="92e5b-110">Called by:</span></span>  <br/> |<span data-ttu-id="92e5b-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="92e5b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="92e5b-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92e5b-112">Parameters</span></span>

 <span data-ttu-id="92e5b-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="92e5b-113">_pvalMv_</span></span>
  
> <span data-ttu-id="92e5b-114">[entrada] Puntero a una [estructura SPropValue](spropvalue.md) que define una propiedad multivalor.</span><span class="sxs-lookup"><span data-stu-id="92e5b-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="92e5b-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="92e5b-115">_pvalSv_</span></span>
  
> <span data-ttu-id="92e5b-116">[entrada] Puntero a una propiedad de un solo valor para recibir datos.</span><span class="sxs-lookup"><span data-stu-id="92e5b-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="92e5b-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="92e5b-117">_uliInst_</span></span>
  
> <span data-ttu-id="92e5b-118">[entrada] El número de instancia, es decir, el elemento de matriz, del valor que se copia de la estructura indicada por el _parámetro pvalMv._</span><span class="sxs-lookup"><span data-stu-id="92e5b-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="92e5b-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92e5b-119">Return value</span></span>

<span data-ttu-id="92e5b-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92e5b-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="92e5b-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92e5b-121">Remarks</span></span>

<span data-ttu-id="92e5b-122">Si el valor copiado es demasiado grande para la memoria asignada, la función **GetInstance** solo copia punteros en lugar de asignar nueva memoria.</span><span class="sxs-lookup"><span data-stu-id="92e5b-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

