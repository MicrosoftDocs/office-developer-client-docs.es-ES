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
ms.openlocfilehash: 37dc92a40043657cb791359d543ef52c77dbd8ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589241"
---
# <a name="ftnegft"></a><span data-ttu-id="1cd95-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="1cd95-103">FtNegFt</span></span>

  
  
<span data-ttu-id="1cd95-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cd95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cd95-105">Calcula el complemento de dos de un entero de 64 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="1cd95-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1cd95-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1cd95-106">Header file:</span></span>  <br/> |<span data-ttu-id="1cd95-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1cd95-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1cd95-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="1cd95-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1cd95-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1cd95-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1cd95-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1cd95-110">Called by:</span></span>  <br/> |<span data-ttu-id="1cd95-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="1cd95-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="1cd95-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cd95-112">Parameters</span></span>

 <span data-ttu-id="1cd95-113">_FT_</span><span class="sxs-lookup"><span data-stu-id="1cd95-113">_ft_</span></span>
  
> <span data-ttu-id="1cd95-114">[entrada] Una estructura [FILETIME](filetime.md) que contiene el entero sin signo de 64 bits que se va a calcular el complemento de dos.</span><span class="sxs-lookup"><span data-stu-id="1cd95-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1cd95-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cd95-115">Return value</span></span>

<span data-ttu-id="1cd95-116">La función **FtNegFt** devuelve una estructura **FILETIME** que contiene el complemento de dos del número entero.</span><span class="sxs-lookup"><span data-stu-id="1cd95-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="1cd95-117">El parámetro de entrada no sufre cambios.</span><span class="sxs-lookup"><span data-stu-id="1cd95-117">The input parameter remains unchanged.</span></span> 
  

