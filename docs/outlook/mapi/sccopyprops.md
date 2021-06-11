---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411011"
---
# <a name="sccopyprops"></a><span data-ttu-id="dfc83-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="dfc83-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="dfc83-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfc83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfc83-105">Copia las propiedades definidas por una matriz de [estructuras SPropValue](spropvalue.md) en un nuevo destino.</span><span class="sxs-lookup"><span data-stu-id="dfc83-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfc83-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="dfc83-106">Header file:</span></span>  <br/> |<span data-ttu-id="dfc83-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="dfc83-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dfc83-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="dfc83-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dfc83-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dfc83-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dfc83-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="dfc83-110">Called by:</span></span>  <br/> |<span data-ttu-id="dfc83-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="dfc83-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="dfc83-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="dfc83-112">Parameters</span></span>

 <span data-ttu-id="dfc83-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="dfc83-113">_cprop_</span></span>
  
> <span data-ttu-id="dfc83-114">[in] Recuento de propiedades que se van a copiar.</span><span class="sxs-lookup"><span data-stu-id="dfc83-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="dfc83-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="dfc83-115">_rgprop_</span></span>
  
> <span data-ttu-id="dfc83-116">[in] Puntero a una matriz de [estructuras SPropValue](spropvalue.md) que definen las propiedades que se van a copiar.</span><span class="sxs-lookup"><span data-stu-id="dfc83-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="dfc83-117">El  _parámetro rgprop_ no tiene que apuntar al principio de la matriz, pero debe apuntar al principio de una de las estructuras **SPropValue** de la matriz.</span><span class="sxs-lookup"><span data-stu-id="dfc83-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="dfc83-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="dfc83-118">_pvDst_</span></span>
  
> <span data-ttu-id="dfc83-119">[in] Puntero a la posición inicial en la memoria a la que esta función copia las propiedades.</span><span class="sxs-lookup"><span data-stu-id="dfc83-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="dfc83-120">_pcb_</span><span class="sxs-lookup"><span data-stu-id="dfc83-120">_pcb_</span></span>
  
> <span data-ttu-id="dfc83-121">[salida] Puntero opcional al tamaño, en bytes, del bloque de memoria señalado por el _parámetro pvDst._</span><span class="sxs-lookup"><span data-stu-id="dfc83-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dfc83-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfc83-122">Return value</span></span>

<span data-ttu-id="dfc83-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="dfc83-123">S_OK</span></span>
  
> <span data-ttu-id="dfc83-124">Las propiedades se copiaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="dfc83-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="dfc83-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dfc83-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="dfc83-126">Se encontró un tipo de propiedad desconocido.</span><span class="sxs-lookup"><span data-stu-id="dfc83-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dfc83-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dfc83-127">Remarks</span></span>

<span data-ttu-id="dfc83-128">La nueva matriz y sus datos residen en un búfer creado con una sola asignación y la función [ScRelocProps](screlocprops.md) se puede usar para ajustar los punteros de las estructuras [SPropValue](spropvalue.md) individuales.</span><span class="sxs-lookup"><span data-stu-id="dfc83-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="dfc83-129">Antes de este ajuste, los punteros son válidos.</span><span class="sxs-lookup"><span data-stu-id="dfc83-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="dfc83-130">**ScCopyProps** mantiene el orden de propiedad original de la matriz de propiedades copiada.</span><span class="sxs-lookup"><span data-stu-id="dfc83-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="dfc83-131">El _parámetro pcb_ es opcional; si no es NULL, se establece en el número de bytes almacenados en el _parámetro pvDst._</span><span class="sxs-lookup"><span data-stu-id="dfc83-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dfc83-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfc83-132">See also</span></span>



[<span data-ttu-id="dfc83-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="dfc83-133">ScDupPropset</span></span>](scduppropset.md)

