---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 13dad61176a877295069317e4a5b51888b01bebb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820661"
---
# <a name="sizedadrlist"></a><span data-ttu-id="cc5f2-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="cc5f2-103">SizedADRLIST</span></span>

<span data-ttu-id="cc5f2-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cc5f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cc5f2-105">Define una estructura de [ADRLIST](adrlist.md) con el nombre especificado que contiene un número especificado de estructuras [ADRENTRY](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="cc5f2-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc5f2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="cc5f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="cc5f2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc5f2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="cc5f2-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="cc5f2-108">Related structure:</span></span>  <br/> |<span data-ttu-id="cc5f2-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="cc5f2-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="cc5f2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc5f2-110">Parameters</span></span>

<span data-ttu-id="cc5f2-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="cc5f2-111">__centries_</span></span>
  
> <span data-ttu-id="cc5f2-112">Recuento de las estructuras **ADRENTRY** que se deben incluir en la nueva estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="cc5f2-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="cc5f2-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="cc5f2-113">__name_</span></span>
  
> <span data-ttu-id="cc5f2-114">Nombre de la nueva estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="cc5f2-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cc5f2-115">Notas</span><span class="sxs-lookup"><span data-stu-id="cc5f2-115">Remarks</span></span>

<span data-ttu-id="cc5f2-116">La macro **SizedADRLIST** le permite definir una lista de destinatarios que tiene límites explícitos cuando se conocen los requisitos de longitud de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cc5f2-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="cc5f2-117">El código siguiente muestra cómo convertir el resultado de la macro **SizedADRLIST** a un puntero de estructura **ADRLIST** :</span><span class="sxs-lookup"><span data-stu-id="cc5f2-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="cc5f2-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="cc5f2-118">See also</span></span>

- [<span data-ttu-id="cc5f2-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="cc5f2-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="cc5f2-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="cc5f2-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="cc5f2-121">Macros relacionadas con las estructuras</span><span class="sxs-lookup"><span data-stu-id="cc5f2-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

