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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327975"
---
# <a name="ftnegft"></a><span data-ttu-id="b67a4-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="b67a4-103">FtNegFt</span></span>

  
  
<span data-ttu-id="b67a4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b67a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b67a4-105">Calcula el complemento de dos de un entero de 64 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="b67a4-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b67a4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b67a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="b67a4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="b67a4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b67a4-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b67a4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b67a4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b67a4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b67a4-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b67a4-110">Called by:</span></span>  <br/> |<span data-ttu-id="b67a4-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="b67a4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="b67a4-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="b67a4-112">Parameters</span></span>

 <span data-ttu-id="b67a4-113">_cm_</span><span class="sxs-lookup"><span data-stu-id="b67a4-113">_ft_</span></span>
  
> <span data-ttu-id="b67a4-114">a Una estructura [FILETIME](filetime.md) que contiene el entero de 64 bits sin signo para calcular el complemento de dos.</span><span class="sxs-lookup"><span data-stu-id="b67a4-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b67a4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b67a4-115">Return value</span></span>

<span data-ttu-id="b67a4-116">La función **FtNegFt** devuelve una estructura **FILETIME** que contiene los dos complementarios del entero.</span><span class="sxs-lookup"><span data-stu-id="b67a4-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="b67a4-117">El parámetro de entrada permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="b67a4-117">The input parameter remains unchanged.</span></span> 
  

