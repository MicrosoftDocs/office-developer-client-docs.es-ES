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
ms.openlocfilehash: ee004bdfb8d13537fd8823225f155223ebc76ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583354"
---
# <a name="sccountprops"></a><span data-ttu-id="aa19b-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="aa19b-103">ScCountProps</span></span>

  
  
<span data-ttu-id="aa19b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa19b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa19b-105">Determina el tamaño, en bytes, de una matriz de valores de propiedad y valida la memoria asociada a la matriz.</span><span class="sxs-lookup"><span data-stu-id="aa19b-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aa19b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="aa19b-106">Header file:</span></span>  <br/> |<span data-ttu-id="aa19b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="aa19b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="aa19b-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="aa19b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="aa19b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="aa19b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="aa19b-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="aa19b-110">Called by:</span></span>  <br/> |<span data-ttu-id="aa19b-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="aa19b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="aa19b-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa19b-112">Parameters</span></span>

 <span data-ttu-id="aa19b-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="aa19b-113">_cprop_</span></span>
  
> <span data-ttu-id="aa19b-114">[entrada] Recuento de propiedades en la matriz indicada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="aa19b-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="aa19b-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="aa19b-115">_rgprop_</span></span>
  
> <span data-ttu-id="aa19b-116">[entrada] Puntero a un rango en una matriz de estructuras [SPropValue](spropvalue.md) que define las propiedades cuyo tamaño es que se determinará.</span><span class="sxs-lookup"><span data-stu-id="aa19b-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="aa19b-117">Este intervalo no se inicia necesariamente al principio de la matriz.</span><span class="sxs-lookup"><span data-stu-id="aa19b-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="aa19b-118">_placa de circuitos impresos_</span><span class="sxs-lookup"><span data-stu-id="aa19b-118">_pcb_</span></span>
  
> <span data-ttu-id="aa19b-119">[out] Puntero opcional para el tamaño, en bytes, de la matriz de propiedad.</span><span class="sxs-lookup"><span data-stu-id="aa19b-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa19b-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa19b-120">Return value</span></span>

<span data-ttu-id="aa19b-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa19b-121">S_OK</span></span> 
  
> <span data-ttu-id="aa19b-122">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="aa19b-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="aa19b-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aa19b-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="aa19b-124">Al menos una propiedad en la matriz de valores de propiedad tiene un identificador de PROP_ID_NULL o PROP_ID_INVALID o la matriz de propiedad contiene una propiedad multivalor sin valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="aa19b-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa19b-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa19b-125">Remarks</span></span>

<span data-ttu-id="aa19b-126">Si se pasa NULL en el parámetro _pcb_ , la función **ScCountProps** valida la matriz de notificaciones, pero recuento no se realiza.</span><span class="sxs-lookup"><span data-stu-id="aa19b-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="aa19b-127">Si se pasa un valor no nulo en _placa de circuitos impresos_, la función **ScCountNotifications** determina el tamaño de la matriz y almacena la causa _placa de circuitos impresos_.</span><span class="sxs-lookup"><span data-stu-id="aa19b-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="aa19b-128">El parámetro _pcb_ debe ser lo suficientemente grande como para contener toda la matriz.</span><span class="sxs-lookup"><span data-stu-id="aa19b-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="aa19b-129">Tal y como lo está contando, **ScCountProps** valida la memoria asociada a la matriz.</span><span class="sxs-lookup"><span data-stu-id="aa19b-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="aa19b-130">**ScCountProps** sólo funciona con las propiedades MAPI sobre qué dispone de información.</span><span class="sxs-lookup"><span data-stu-id="aa19b-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aa19b-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="aa19b-131">See also</span></span>



[<span data-ttu-id="aa19b-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="aa19b-132">PropCopyMore</span></span>](propcopymore.md)

