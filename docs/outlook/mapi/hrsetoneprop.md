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
ms.openlocfilehash: 31d2be027ef3b58fdd44e71c922677164d352feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569130"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="d17e4-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="d17e4-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="d17e4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d17e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d17e4-105">Establece o cambia el valor de una propiedad única en una interfaz (propiedad), es decir, una interfaz que se deriva de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d17e4-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d17e4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d17e4-106">Header file:</span></span>  <br/> |<span data-ttu-id="d17e4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d17e4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d17e4-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="d17e4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d17e4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d17e4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d17e4-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d17e4-110">Called by:</span></span>  <br/> |<span data-ttu-id="d17e4-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d17e4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="d17e4-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d17e4-112">Parameters</span></span>

 <span data-ttu-id="d17e4-113">_médico principal_</span><span class="sxs-lookup"><span data-stu-id="d17e4-113">_pmp_</span></span>
  
> <span data-ttu-id="d17e4-114">[entrada] Puntero a una interfaz de [IMAPIProp](imapipropiunknown.md) en el que se puede establecer o cambiar el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d17e4-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="d17e4-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="d17e4-115">_pprop_</span></span>
  
> <span data-ttu-id="d17e4-116">[entrada] Puntero a la estructura de [SPropValue](spropvalue.md) define el valor que se establecerá en la propiedad _médico principal_ .</span><span class="sxs-lookup"><span data-stu-id="d17e4-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d17e4-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d17e4-117">Return value</span></span>

<span data-ttu-id="d17e4-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d17e4-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d17e4-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d17e4-119">Remarks</span></span>

<span data-ttu-id="d17e4-120">A diferencia del método [IMAPIProp::SetProps](imapiprop-setprops.md) , la función **HrSetOneProp** no devuelve nunca si hay alguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="d17e4-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="d17e4-121">Ya que se establece sólo una propiedad, que simplemente se realiza correctamente o se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d17e4-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="d17e4-122">Para configurar o cambiar las propiedades de varios, **SetProps** es más rápido.</span><span class="sxs-lookup"><span data-stu-id="d17e4-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="d17e4-123">Puede recuperar una sola propiedad con la función [HrGetOneProp](hrgetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="d17e4-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

