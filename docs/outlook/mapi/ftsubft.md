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
ms.openlocfilehash: ad561bd3be7fd0c9f25c11875f62667563dfcbe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578265"
---
# <a name="ftsubft"></a><span data-ttu-id="7e3c6-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="7e3c6-103">FtSubFt</span></span>

  
  
<span data-ttu-id="7e3c6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e3c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e3c6-105">Resta un entero sin signo de 64 bits de otro.</span><span class="sxs-lookup"><span data-stu-id="7e3c6-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7e3c6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7e3c6-106">Header file:</span></span>  <br/> |<span data-ttu-id="7e3c6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7e3c6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7e3c6-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="7e3c6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7e3c6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7e3c6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7e3c6-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7e3c6-110">Called by:</span></span>  <br/> |<span data-ttu-id="7e3c6-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="7e3c6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="7e3c6-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e3c6-112">Parameters</span></span>

 <span data-ttu-id="7e3c6-113">_Minuendo_</span><span class="sxs-lookup"><span data-stu-id="7e3c6-113">_Minuend_</span></span>
  
> <span data-ttu-id="7e3c6-114">[entrada] Una estructura [FILETIME](filetime.md) que contiene el entero de 64 bits sin signo desde la que el valor en el parámetro _sustraendo_ es que se va a restar.</span><span class="sxs-lookup"><span data-stu-id="7e3c6-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="7e3c6-115">_Sustraendo_</span><span class="sxs-lookup"><span data-stu-id="7e3c6-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="7e3c6-116">[entrada] Una estructura **FILETIME** que contiene el entero sin signo de 64 bits que se resta el valor indicado por el parámetro _minuendo_ .</span><span class="sxs-lookup"><span data-stu-id="7e3c6-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7e3c6-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e3c6-117">Return value</span></span>

<span data-ttu-id="7e3c6-118">La función **FtSubFt** devuelve una estructura **FILETIME** que contiene el resultado de la resta.</span><span class="sxs-lookup"><span data-stu-id="7e3c6-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="7e3c6-119">No se modifican los dos parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="7e3c6-119">The two input parameters remain unchanged.</span></span> 
  

