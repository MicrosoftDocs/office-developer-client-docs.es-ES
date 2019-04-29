---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 37e6560d859ce4731b7a06e571eb38eb160c3686
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417661"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="b4512-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="b4512-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="b4512-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4512-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4512-105">Establece o cambia el valor de una propiedad única en una interfaz de propiedades, es decir, una interfaz derivada de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="b4512-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4512-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b4512-106">Header file:</span></span>  <br/> |<span data-ttu-id="b4512-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="b4512-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b4512-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b4512-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b4512-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b4512-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b4512-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b4512-110">Called by:</span></span>  <br/> |<span data-ttu-id="b4512-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="b4512-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="b4512-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="b4512-112">Parameters</span></span>

 <span data-ttu-id="b4512-113">_proveedor_</span><span class="sxs-lookup"><span data-stu-id="b4512-113">_pmp_</span></span>
  
> <span data-ttu-id="b4512-114">a Puntero a una interfaz de [IMAPIProp](imapipropiunknown.md) en la que se va a establecer o cambiar el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b4512-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="b4512-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="b4512-115">_pprop_</span></span>
  
> <span data-ttu-id="b4512-116">a Puntero a la estructura [SPropValue](spropvalue.md) que define el valor que se va a establecer en la propiedad _PMP_ .</span><span class="sxs-lookup"><span data-stu-id="b4512-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b4512-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4512-117">Return value</span></span>

<span data-ttu-id="b4512-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b4512-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4512-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b4512-119">Remarks</span></span>

<span data-ttu-id="b4512-120">A diferencia del método [IMAPIProp:: SetProps](imapiprop-setprops.md) , la función **HrSetOneProp** nunca devuelve ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="b4512-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="b4512-121">Dado que sólo establece una propiedad, simplemente se realiza correctamente o produce un error.</span><span class="sxs-lookup"><span data-stu-id="b4512-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="b4512-122">Para establecer o cambiar varias propiedades, **SetProps** es más rápido.</span><span class="sxs-lookup"><span data-stu-id="b4512-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="b4512-123">Puede recuperar una sola propiedad con la función [HrGetOneProp](hrgetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="b4512-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

