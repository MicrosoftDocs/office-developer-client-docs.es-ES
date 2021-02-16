---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cc1547ad7d881b707825630f96987d4c40ad4863
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416905"
---
# <a name="ulpropsize"></a><span data-ttu-id="8cb96-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="8cb96-103">UlPropSize</span></span>

  
  
<span data-ttu-id="8cb96-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cb96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8cb96-105">Devuelve el tamaño de un solo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8cb96-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8cb96-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8cb96-106">Header file:</span></span>  <br/> |<span data-ttu-id="8cb96-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8cb96-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8cb96-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="8cb96-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8cb96-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8cb96-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8cb96-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="8cb96-110">Called by:</span></span>  <br/> |<span data-ttu-id="8cb96-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="8cb96-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="8cb96-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cb96-112">Parameters</span></span>

 <span data-ttu-id="8cb96-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="8cb96-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="8cb96-114">[entrada] Puntero a una [estructura SPropValue](spropvalue.md) que define la propiedad que se va a medir.</span><span class="sxs-lookup"><span data-stu-id="8cb96-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8cb96-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cb96-115">Return value</span></span>

<span data-ttu-id="8cb96-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb96-116">S_OK</span></span> 
  
> <span data-ttu-id="8cb96-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="8cb96-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="8cb96-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="8cb96-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="8cb96-119">Un error de origen inesperado o desconocido impidió que se completara la operación.</span><span class="sxs-lookup"><span data-stu-id="8cb96-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8cb96-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8cb96-120">Remarks</span></span>

<span data-ttu-id="8cb96-121">La **función UlPropSize** devuelve el tamaño, en bytes, del valor de propiedad de la propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="8cb96-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="8cb96-122">Ignora el tamaño del resto de la estructura **SPropValue.**</span><span class="sxs-lookup"><span data-stu-id="8cb96-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

