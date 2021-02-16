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
# <a name="hrsetoneprop"></a><span data-ttu-id="38a12-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="38a12-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="38a12-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38a12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38a12-105">Establece o cambia el valor de una sola propiedad en una interfaz de propiedades, es decir, una interfaz derivada de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="38a12-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38a12-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="38a12-106">Header file:</span></span>  <br/> |<span data-ttu-id="38a12-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="38a12-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="38a12-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="38a12-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="38a12-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="38a12-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="38a12-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="38a12-110">Called by:</span></span>  <br/> |<span data-ttu-id="38a12-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="38a12-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="38a12-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38a12-112">Parameters</span></span>

 <span data-ttu-id="38a12-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="38a12-113">_pmp_</span></span>
  
> <span data-ttu-id="38a12-114">[entrada] Puntero a una [interfaz IMAPIProp](imapipropiunknown.md) en la que se va a establecer o cambiar el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="38a12-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="38a12-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="38a12-115">_pprop_</span></span>
  
> <span data-ttu-id="38a12-116">[entrada] Puntero a la [estructura SPropValue](spropvalue.md) que define el valor que se va a establecer en la _propiedad pmp._</span><span class="sxs-lookup"><span data-stu-id="38a12-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="38a12-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38a12-117">Return value</span></span>

<span data-ttu-id="38a12-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="38a12-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38a12-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38a12-119">Remarks</span></span>

<span data-ttu-id="38a12-120">A diferencia [del método IMAPIProp::SetProps,](imapiprop-setprops.md) la función **HrSetOneProp** nunca devuelve ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="38a12-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="38a12-121">Dado que establece solo una propiedad, simplemente se realiza correctamente o se produce un error.</span><span class="sxs-lookup"><span data-stu-id="38a12-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="38a12-122">Para establecer o cambiar varias propiedades, **SetProps** es más rápido.</span><span class="sxs-lookup"><span data-stu-id="38a12-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="38a12-123">Puede recuperar una sola propiedad con la [función HrGetOneProp.](hrgetoneprop.md)</span><span class="sxs-lookup"><span data-stu-id="38a12-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

