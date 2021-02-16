---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423387"
---
# <a name="ftnegft"></a><span data-ttu-id="e1bbf-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="e1bbf-103">FtNegFt</span></span>

  
  
<span data-ttu-id="e1bbf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1bbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1bbf-105">Calcula el complemento de los dos de un entero de 64 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="e1bbf-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1bbf-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e1bbf-106">Header file:</span></span>  <br/> |<span data-ttu-id="e1bbf-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e1bbf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e1bbf-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e1bbf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e1bbf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e1bbf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e1bbf-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e1bbf-110">Called by:</span></span>  <br/> |<span data-ttu-id="e1bbf-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="e1bbf-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="e1bbf-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1bbf-112">Parameters</span></span>

 <span data-ttu-id="e1bbf-113">_ft_</span><span class="sxs-lookup"><span data-stu-id="e1bbf-113">_ft_</span></span>
  
> <span data-ttu-id="e1bbf-114">[entrada] Estructura [FILETIME](filetime.md) que contiene el entero de 64 bits sin signo para el que se va a calcular el complemento de los dos.</span><span class="sxs-lookup"><span data-stu-id="e1bbf-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e1bbf-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1bbf-115">Return value</span></span>

<span data-ttu-id="e1bbf-116">La **función FtNegFt** devuelve una **estructura FILETIME** que contiene el complemento de los dos enteros.</span><span class="sxs-lookup"><span data-stu-id="e1bbf-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="e1bbf-117">El parámetro de entrada no cambia.</span><span class="sxs-lookup"><span data-stu-id="e1bbf-117">The input parameter remains unchanged.</span></span> 
  

