---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404977"
---
# <a name="sccountprops"></a><span data-ttu-id="3b77a-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="3b77a-103">ScCountProps</span></span>

  
  
<span data-ttu-id="3b77a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b77a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b77a-105">Determina el tamaño, en bytes, de una matriz de valores de propiedad y valida la memoria asociada a la matriz.</span><span class="sxs-lookup"><span data-stu-id="3b77a-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b77a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3b77a-106">Header file:</span></span>  <br/> |<span data-ttu-id="3b77a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3b77a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3b77a-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="3b77a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3b77a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3b77a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3b77a-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="3b77a-110">Called by:</span></span>  <br/> |<span data-ttu-id="3b77a-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="3b77a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="3b77a-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="3b77a-112">Parameters</span></span>

 <span data-ttu-id="3b77a-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="3b77a-113">_cprop_</span></span>
  
> <span data-ttu-id="3b77a-114">[in] Recuento de propiedades en la matriz indicada por el _parámetro rgprop._</span><span class="sxs-lookup"><span data-stu-id="3b77a-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="3b77a-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="3b77a-115">_rgprop_</span></span>
  
> <span data-ttu-id="3b77a-116">[in] Puntero a un rango de una matriz de [estructuras SPropValue](spropvalue.md) que define las propiedades cuyo tamaño se va a determinar.</span><span class="sxs-lookup"><span data-stu-id="3b77a-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="3b77a-117">Este intervalo no se inicia necesariamente al principio de la matriz.</span><span class="sxs-lookup"><span data-stu-id="3b77a-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="3b77a-118">_pcb_</span><span class="sxs-lookup"><span data-stu-id="3b77a-118">_pcb_</span></span>
  
> <span data-ttu-id="3b77a-119">[salida] Puntero opcional al tamaño, en bytes, de la matriz de propiedades.</span><span class="sxs-lookup"><span data-stu-id="3b77a-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3b77a-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b77a-120">Return value</span></span>

<span data-ttu-id="3b77a-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b77a-121">S_OK</span></span> 
  
> <span data-ttu-id="3b77a-122">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="3b77a-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="3b77a-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3b77a-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="3b77a-124">Al menos una propiedad de la matriz de valores de propiedad tiene un identificador de PROP_ID_NULL o PROP_ID_INVALID, o la matriz de propiedades contiene una propiedad multivalor sin valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="3b77a-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b77a-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b77a-125">Remarks</span></span>

<span data-ttu-id="3b77a-126">Si se pasa NULL en el  _parámetro pcb,_ la función **ScCountProps** valida la matriz de notificaciones, pero no se realiza ningún recuento.</span><span class="sxs-lookup"><span data-stu-id="3b77a-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="3b77a-127">Si se pasa un valor que no es nulo en  _pcb_, la función **ScCountNotifications** determina el tamaño de la matriz y almacena la  _causa pcb_.</span><span class="sxs-lookup"><span data-stu-id="3b77a-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="3b77a-128">El  _parámetro pcb_ debe ser lo suficientemente grande como para contener toda la matriz.</span><span class="sxs-lookup"><span data-stu-id="3b77a-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="3b77a-129">Al contar, **ScCountProps** valida la memoria asociada a la matriz.</span><span class="sxs-lookup"><span data-stu-id="3b77a-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="3b77a-130">**ScCountProps solo** funciona con propiedades sobre las que MAPI tiene información.</span><span class="sxs-lookup"><span data-stu-id="3b77a-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b77a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b77a-131">See also</span></span>



[<span data-ttu-id="3b77a-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="3b77a-132">PropCopyMore</span></span>](propcopymore.md)

