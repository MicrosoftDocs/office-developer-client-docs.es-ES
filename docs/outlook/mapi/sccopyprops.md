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
ms.openlocfilehash: 979415f1d792f92e593a7073cc84cfd6ba832b6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820568"
---
# <a name="sccopyprops"></a><span data-ttu-id="6317d-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="6317d-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="6317d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6317d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6317d-105">Copias de las propiedades definidas por una matriz de estructuras [SPropValue](spropvalue.md) a un nuevo destino.</span><span class="sxs-lookup"><span data-stu-id="6317d-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6317d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6317d-106">Header file:</span></span>  <br/> |<span data-ttu-id="6317d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6317d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6317d-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="6317d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6317d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6317d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6317d-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="6317d-110">Called by:</span></span>  <br/> |<span data-ttu-id="6317d-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="6317d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="6317d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6317d-112">Parameters</span></span>

 <span data-ttu-id="6317d-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="6317d-113">_cprop_</span></span>
  
> <span data-ttu-id="6317d-114">[entrada] Recuento de propiedades que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="6317d-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="6317d-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="6317d-115">_rgprop_</span></span>
  
> <span data-ttu-id="6317d-116">[entrada] Puntero a una matriz de estructuras [SPropValue](spropvalue.md) que definen las propiedades que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="6317d-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="6317d-117">El parámetro _rgprop_ no tiene para que apunte al principio de la matriz, pero debe apuntar al principio de una de las estructuras de **SPropValue** en la matriz.</span><span class="sxs-lookup"><span data-stu-id="6317d-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="6317d-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="6317d-118">_pvDst_</span></span>
  
> <span data-ttu-id="6317d-119">[entrada] Puntero a la posición inicial en la memoria a la que esta función copia las propiedades.</span><span class="sxs-lookup"><span data-stu-id="6317d-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="6317d-120">_placa de circuitos impresos_</span><span class="sxs-lookup"><span data-stu-id="6317d-120">_pcb_</span></span>
  
> <span data-ttu-id="6317d-121">[out] Puntero opcional para el tamaño, en bytes, del bloque de memoria indicada por el parámetro _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="6317d-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6317d-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6317d-122">Return value</span></span>

<span data-ttu-id="6317d-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="6317d-123">S_OK</span></span>
  
> <span data-ttu-id="6317d-124">Las propiedades se han copiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6317d-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="6317d-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6317d-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="6317d-126">Se encontró un tipo de propiedad desconocido.</span><span class="sxs-lookup"><span data-stu-id="6317d-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6317d-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6317d-127">Remarks</span></span>

<span data-ttu-id="6317d-128">La nueva matriz y sus datos residen en un búfer creado con una única asignación, y la función [ScRelocProps](screlocprops.md) puede usarse para ajustar los punteros en las estructuras de [SPropValue](spropvalue.md) individuales.</span><span class="sxs-lookup"><span data-stu-id="6317d-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="6317d-129">Antes de este ajuste, los punteros son válidos.</span><span class="sxs-lookup"><span data-stu-id="6317d-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="6317d-130">**ScCopyProps** mantiene el orden de propiedad original de la matriz de propiedad copiados.</span><span class="sxs-lookup"><span data-stu-id="6317d-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="6317d-131">El parámetro _pcb_ es opcional; Si no es NULL, se establece el número de bytes que se almacenan en el parámetro _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="6317d-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6317d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6317d-132">See also</span></span>



[<span data-ttu-id="6317d-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="6317d-133">ScDupPropset</span></span>](scduppropset.md)

