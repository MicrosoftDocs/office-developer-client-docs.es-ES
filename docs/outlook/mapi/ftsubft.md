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
ms.openlocfilehash: 954630b0b92772d961dc61084c28a9ab419e4c2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816900"
---
# <a name="ftsubft"></a><span data-ttu-id="8c36a-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="8c36a-103">FtSubFt</span></span>

  
  
<span data-ttu-id="8c36a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c36a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c36a-105">Resta un entero sin signo de 64 bits de otro.</span><span class="sxs-lookup"><span data-stu-id="8c36a-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c36a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8c36a-106">Header file:</span></span>  <br/> |<span data-ttu-id="8c36a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="8c36a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8c36a-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="8c36a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8c36a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8c36a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8c36a-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="8c36a-110">Called by:</span></span>  <br/> |<span data-ttu-id="8c36a-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="8c36a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="8c36a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c36a-112">Parameters</span></span>

 <span data-ttu-id="8c36a-113">_Minuendo_</span><span class="sxs-lookup"><span data-stu-id="8c36a-113">_Minuend_</span></span>
  
> <span data-ttu-id="8c36a-114">[entrada] Una estructura [FILETIME](filetime.md) que contiene el entero de 64 bits sin signo desde la que el valor en el parámetro _sustraendo_ es que se va a restar.</span><span class="sxs-lookup"><span data-stu-id="8c36a-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="8c36a-115">_Sustraendo_</span><span class="sxs-lookup"><span data-stu-id="8c36a-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="8c36a-116">[entrada] Una estructura **FILETIME** que contiene el entero sin signo de 64 bits que se resta el valor indicado por el parámetro _minuendo_ .</span><span class="sxs-lookup"><span data-stu-id="8c36a-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8c36a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c36a-117">Return value</span></span>

<span data-ttu-id="8c36a-118">La función **FtSubFt** devuelve una estructura **FILETIME** que contiene el resultado de la resta.</span><span class="sxs-lookup"><span data-stu-id="8c36a-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="8c36a-119">No se modifican los dos parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="8c36a-119">The two input parameters remain unchanged.</span></span> 
  

