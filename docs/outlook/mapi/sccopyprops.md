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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351334"
---
# <a name="sccopyprops"></a><span data-ttu-id="5eb38-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="5eb38-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="5eb38-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5eb38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5eb38-105">Copia las propiedades definidas por una matriz de estructuras [SPropValue](spropvalue.md) en un nuevo destino.</span><span class="sxs-lookup"><span data-stu-id="5eb38-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5eb38-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5eb38-106">Header file:</span></span>  <br/> |<span data-ttu-id="5eb38-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="5eb38-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5eb38-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5eb38-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5eb38-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5eb38-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5eb38-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5eb38-110">Called by:</span></span>  <br/> |<span data-ttu-id="5eb38-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="5eb38-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="5eb38-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="5eb38-112">Parameters</span></span>

 <span data-ttu-id="5eb38-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="5eb38-113">_cprop_</span></span>
  
> <span data-ttu-id="5eb38-114">a Número de propiedades que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="5eb38-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="5eb38-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="5eb38-115">_rgprop_</span></span>
  
> <span data-ttu-id="5eb38-116">a Puntero a una matriz de estructuras [SPropValue](spropvalue.md) que definen las propiedades que se van a copiar.</span><span class="sxs-lookup"><span data-stu-id="5eb38-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="5eb38-117">El parámetro _rgprop_ no tiene que apuntar al principio de la matriz, pero debe apuntar al principio de una de las estructuras **SPropValue** de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5eb38-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="5eb38-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="5eb38-118">_pvDst_</span></span>
  
> <span data-ttu-id="5eb38-119">a Puntero a la posición inicial en la memoria a la que esta función copia las propiedades.</span><span class="sxs-lookup"><span data-stu-id="5eb38-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="5eb38-120">_impreso_</span><span class="sxs-lookup"><span data-stu-id="5eb38-120">_pcb_</span></span>
  
> <span data-ttu-id="5eb38-121">contempla Puntero opcional al tamaño, en bytes, del bloque de memoria al que apunta el parámetro _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="5eb38-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5eb38-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5eb38-122">Return value</span></span>

<span data-ttu-id="5eb38-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="5eb38-123">S_OK</span></span>
  
> <span data-ttu-id="5eb38-124">Las propiedades se han copiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5eb38-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="5eb38-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5eb38-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="5eb38-126">Se encontró un tipo de propiedad desconocido.</span><span class="sxs-lookup"><span data-stu-id="5eb38-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5eb38-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5eb38-127">Remarks</span></span>

<span data-ttu-id="5eb38-128">La nueva matriz y sus datos residen en un búfer creado con una única asignación, y la función [ScRelocProps](screlocprops.md) se puede usar para ajustar los punteros en las estructuras individuales de [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="5eb38-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="5eb38-129">Antes de este ajuste, los punteros son válidos.</span><span class="sxs-lookup"><span data-stu-id="5eb38-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="5eb38-130">**ScCopyProps** mantiene el orden de propiedades original de la matriz de propiedades copiada.</span><span class="sxs-lookup"><span data-stu-id="5eb38-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="5eb38-131">El parámetro _PCB_ es opcional; Si no es NULL, se establece en el número de bytes almacenados en el parámetro _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="5eb38-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5eb38-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="5eb38-132">See also</span></span>



[<span data-ttu-id="5eb38-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="5eb38-133">ScDupPropset</span></span>](scduppropset.md)

