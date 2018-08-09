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
ms.openlocfilehash: e0e1535a770d4f1b437faf6a90c5f6415f6000ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816897"
---
# <a name="ftaddft"></a><span data-ttu-id="7239a-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="7239a-103">FtAddFt</span></span>

  
  
<span data-ttu-id="7239a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7239a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7239a-105">Agrega un entero de 64 bits sin signo a otra.</span><span class="sxs-lookup"><span data-stu-id="7239a-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7239a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7239a-106">Header file:</span></span>  <br/> |<span data-ttu-id="7239a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7239a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7239a-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="7239a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7239a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7239a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7239a-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7239a-110">Called by:</span></span>  <br/> |<span data-ttu-id="7239a-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="7239a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="7239a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7239a-112">Parameters</span></span>

 <span data-ttu-id="7239a-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="7239a-113">_Addend1_</span></span>
  
> <span data-ttu-id="7239a-114">[entrada] Una estructura [FILETIME](filetime.md) que contiene el primer entero de 64 bits sin signo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="7239a-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="7239a-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="7239a-115">_Addend2_</span></span>
  
> <span data-ttu-id="7239a-116">[entrada] Una estructura **FILETIME** que contiene el segundo entero de 64 bits sin signo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="7239a-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7239a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7239a-117">Return value</span></span>

<span data-ttu-id="7239a-118">La función **FtAddFt** devuelve una estructura **FILETIME** que contiene la suma de los dos números enteros.</span><span class="sxs-lookup"><span data-stu-id="7239a-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="7239a-119">No se modifican los dos parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="7239a-119">The two input parameters remain unchanged.</span></span> 
  

