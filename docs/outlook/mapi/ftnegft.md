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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e26acb8415df007a7f3fb5901521da7222ae40ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816905"
---
# <a name="ftnegft"></a><span data-ttu-id="a3193-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="a3193-103">FtNegFt</span></span>

  
  
<span data-ttu-id="a3193-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3193-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3193-105">Calcula el complemento de dos de un entero de 64 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="a3193-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3193-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a3193-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3193-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a3193-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a3193-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="a3193-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3193-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a3193-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a3193-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a3193-110">Called by:</span></span>  <br/> |<span data-ttu-id="a3193-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="a3193-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="a3193-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3193-112">Parameters</span></span>

 <span data-ttu-id="a3193-113">_FT_</span><span class="sxs-lookup"><span data-stu-id="a3193-113">_ft_</span></span>
  
> <span data-ttu-id="a3193-114">[entrada] Una estructura [FILETIME](filetime.md) que contiene el entero sin signo de 64 bits que se va a calcular el complemento de dos.</span><span class="sxs-lookup"><span data-stu-id="a3193-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a3193-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3193-115">Return value</span></span>

<span data-ttu-id="a3193-116">La función **FtNegFt** devuelve una estructura **FILETIME** que contiene el complemento de dos del número entero.</span><span class="sxs-lookup"><span data-stu-id="a3193-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="a3193-117">El parámetro de entrada no sufre cambios.</span><span class="sxs-lookup"><span data-stu-id="a3193-117">The input parameter remains unchanged.</span></span> 
  

