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
ms.openlocfilehash: c4e5d2847b53988fb75e23fc6c4dfc386ea678f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579266"
---
# <a name="getinstance"></a><span data-ttu-id="ae0f9-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="ae0f9-103">GetInstance</span></span>

  
  
<span data-ttu-id="ae0f9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae0f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae0f9-105">Copia un valor dentro de una propiedad multivalor a una propiedad de un solo valor del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="ae0f9-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae0f9-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ae0f9-106">Header file:</span></span>  <br/> |<span data-ttu-id="ae0f9-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="ae0f9-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="ae0f9-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="ae0f9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ae0f9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ae0f9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ae0f9-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ae0f9-110">Called by:</span></span>  <br/> |<span data-ttu-id="ae0f9-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="ae0f9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="ae0f9-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae0f9-112">Parameters</span></span>

 <span data-ttu-id="ae0f9-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="ae0f9-113">_pvalMv_</span></span>
  
> <span data-ttu-id="ae0f9-114">[entrada] Puntero a una estructura de [SPropValue](spropvalue.md) definir una propiedad multivalor.</span><span class="sxs-lookup"><span data-stu-id="ae0f9-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="ae0f9-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="ae0f9-115">_pvalSv_</span></span>
  
> <span data-ttu-id="ae0f9-116">[entrada] Puntero a una propiedad de un solo valor para recibir datos.</span><span class="sxs-lookup"><span data-stu-id="ae0f9-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="ae0f9-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="ae0f9-117">_uliInst_</span></span>
  
> <span data-ttu-id="ae0f9-118">[entrada] El número de instancia, que es, el elemento de la matriz, del valor que se copió desde la estructura indicada por el parámetro _pvalMv_ .</span><span class="sxs-lookup"><span data-stu-id="ae0f9-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ae0f9-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae0f9-119">Return value</span></span>

<span data-ttu-id="ae0f9-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae0f9-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae0f9-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae0f9-121">Remarks</span></span>

<span data-ttu-id="ae0f9-122">Si el valor que se copia es demasiado grande para la memoria asignada, la función **GetInstance** sólo copia punteros en lugar de asignar memoria nueva.</span><span class="sxs-lookup"><span data-stu-id="ae0f9-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

