---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300395"
---
# <a name="ftsubft"></a><span data-ttu-id="f7148-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="f7148-103">FtSubFt</span></span>

  
  
<span data-ttu-id="f7148-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7148-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7148-105">Resta un entero de 64 bits sin signo de otro.</span><span class="sxs-lookup"><span data-stu-id="f7148-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7148-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f7148-106">Header file:</span></span>  <br/> |<span data-ttu-id="f7148-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="f7148-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f7148-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f7148-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f7148-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f7148-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f7148-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f7148-110">Called by:</span></span>  <br/> |<span data-ttu-id="f7148-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="f7148-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="f7148-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="f7148-112">Parameters</span></span>

 <span data-ttu-id="f7148-113">_Minu_</span><span class="sxs-lookup"><span data-stu-id="f7148-113">_Minuend_</span></span>
  
> <span data-ttu-id="f7148-114">a Una estructura [FILETIME](filetime.md) que contiene el entero de 64 bits sin signo desde el que se resta el valor en el parámetro _sustraendo_ .</span><span class="sxs-lookup"><span data-stu-id="f7148-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="f7148-115">_Stra_</span><span class="sxs-lookup"><span data-stu-id="f7148-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="f7148-116">a Una estructura **FILETIME** que contiene el entero de 64 bits sin signo que se resta del valor indicado por el parámetro _Minus_ .</span><span class="sxs-lookup"><span data-stu-id="f7148-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f7148-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7148-117">Return value</span></span>

<span data-ttu-id="f7148-118">La función **FtSubFt** devuelve una estructura **FILETIME** que contiene el resultado de la resta.</span><span class="sxs-lookup"><span data-stu-id="f7148-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="f7148-119">Los dos parámetros de entrada permanecen sin cambios.</span><span class="sxs-lookup"><span data-stu-id="f7148-119">The two input parameters remain unchanged.</span></span> 
  

