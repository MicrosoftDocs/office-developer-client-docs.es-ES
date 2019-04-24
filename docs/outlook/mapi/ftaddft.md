---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328010"
---
# <a name="ftaddft"></a><span data-ttu-id="325c4-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="325c4-103">FtAddFt</span></span>

  
  
<span data-ttu-id="325c4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="325c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="325c4-105">Agrega un entero de 64 bits sin signo a otro.</span><span class="sxs-lookup"><span data-stu-id="325c4-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="325c4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="325c4-106">Header file:</span></span>  <br/> |<span data-ttu-id="325c4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="325c4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="325c4-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="325c4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="325c4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="325c4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="325c4-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="325c4-110">Called by:</span></span>  <br/> |<span data-ttu-id="325c4-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="325c4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="325c4-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="325c4-112">Parameters</span></span>

 <span data-ttu-id="325c4-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="325c4-113">_Addend1_</span></span>
  
> <span data-ttu-id="325c4-114">a Una estructura [FILETIME](filetime.md) que contiene el primer entero de 64 bits sin signo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="325c4-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="325c4-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="325c4-115">_Addend2_</span></span>
  
> <span data-ttu-id="325c4-116">a Una estructura **FILETIME** que contiene el segundo entero de 64 bits sin signo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="325c4-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="325c4-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="325c4-117">Return value</span></span>

<span data-ttu-id="325c4-118">La función **FtAddFt** devuelve una estructura **FILETIME** que contiene la suma de los dos enteros.</span><span class="sxs-lookup"><span data-stu-id="325c4-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="325c4-119">Los dos parámetros de entrada permanecen sin cambios.</span><span class="sxs-lookup"><span data-stu-id="325c4-119">The two input parameters remain unchanged.</span></span> 
  

