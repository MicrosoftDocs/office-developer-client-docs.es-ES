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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 97dad50fed4179526e46381c4d9ea9d12d568377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820600"
---
# <a name="sccountprops"></a><span data-ttu-id="5e7db-103">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="5e7db-103">ScCountProps</span></span>

  
  
<span data-ttu-id="5e7db-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e7db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e7db-105">Determina el tamaño, en bytes, de una matriz de valores de propiedad y valida la memoria asociada a la matriz.</span><span class="sxs-lookup"><span data-stu-id="5e7db-105">Determines the size, in bytes, of a property value array and validates the memory associated with the array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5e7db-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5e7db-106">Header file:</span></span>  <br/> |<span data-ttu-id="5e7db-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5e7db-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5e7db-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="5e7db-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5e7db-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5e7db-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5e7db-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5e7db-110">Called by:</span></span>  <br/> |<span data-ttu-id="5e7db-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="5e7db-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="5e7db-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e7db-112">Parameters</span></span>

 <span data-ttu-id="5e7db-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="5e7db-113">_cprop_</span></span>
  
> <span data-ttu-id="5e7db-114">[entrada] Recuento de propiedades en la matriz indicada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="5e7db-114">[in] Count of properties in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="5e7db-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="5e7db-115">_rgprop_</span></span>
  
> <span data-ttu-id="5e7db-116">[entrada] Puntero a un rango en una matriz de estructuras [SPropValue](spropvalue.md) que define las propiedades cuyo tamaño es que se determinará.</span><span class="sxs-lookup"><span data-stu-id="5e7db-116">[in] Pointer to a range in an array of [SPropValue](spropvalue.md) structures that defines the properties whose size is to be determined.</span></span> <span data-ttu-id="5e7db-117">Este intervalo no se inicia necesariamente al principio de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5e7db-117">This range does not necessarily start at the beginning of the array.</span></span> 
    
 <span data-ttu-id="5e7db-118">_placa de circuitos impresos_</span><span class="sxs-lookup"><span data-stu-id="5e7db-118">_pcb_</span></span>
  
> <span data-ttu-id="5e7db-119">[out] Puntero opcional para el tamaño, en bytes, de la matriz de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5e7db-119">[out] Optional pointer to the size, in bytes, of the property array.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e7db-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e7db-120">Return value</span></span>

<span data-ttu-id="5e7db-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e7db-121">S_OK</span></span> 
  
> <span data-ttu-id="5e7db-122">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="5e7db-122">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="5e7db-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5e7db-123">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="5e7db-124">Al menos una propiedad en la matriz de valores de propiedad tiene un identificador de PROP_ID_NULL o PROP_ID_INVALID o la matriz de propiedad contiene una propiedad multivalor sin valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5e7db-124">At least one property in the property value array has an identifier of PROP_ID_NULL or PROP_ID_INVALID, or the property array contains a multivalued property with no property values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e7db-125">Notas</span><span class="sxs-lookup"><span data-stu-id="5e7db-125">Remarks</span></span>

<span data-ttu-id="5e7db-126">Si se pasa NULL en el parámetro _pcb_ , la función **ScCountProps** valida la matriz de notificaciones, pero recuento no se realiza.</span><span class="sxs-lookup"><span data-stu-id="5e7db-126">If NULL is passed in the  _pcb_ parameter, the **ScCountProps** function validates the array of notifications but no counting is done.</span></span> <span data-ttu-id="5e7db-127">Si se pasa un valor no nulo en _placa de circuitos impresos_, la función **ScCountNotifications** determina el tamaño de la matriz y almacena la causa _placa de circuitos impresos_.</span><span class="sxs-lookup"><span data-stu-id="5e7db-127">If a non-null value is passed in  _pcb_, the **ScCountNotifications** function determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="5e7db-128">El parámetro _pcb_ debe ser lo suficientemente grande como para contener toda la matriz.</span><span class="sxs-lookup"><span data-stu-id="5e7db-128">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  
<span data-ttu-id="5e7db-129">Tal y como lo está contando, **ScCountProps** valida la memoria asociada a la matriz.</span><span class="sxs-lookup"><span data-stu-id="5e7db-129">As it is counting, **ScCountProps** validates the memory associated with the array.</span></span> <span data-ttu-id="5e7db-130">**ScCountProps** sólo funciona con las propiedades MAPI sobre qué dispone de información.</span><span class="sxs-lookup"><span data-stu-id="5e7db-130">**ScCountProps** only works with properties about which MAPI has information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e7db-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="5e7db-131">See also</span></span>



[<span data-ttu-id="5e7db-132">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="5e7db-132">PropCopyMore</span></span>](propcopymore.md)

