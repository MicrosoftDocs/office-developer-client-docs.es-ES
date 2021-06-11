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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423464"
---
# <a name="sizedadrlist"></a><span data-ttu-id="7030f-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="7030f-103">SizedADRLIST</span></span>

<span data-ttu-id="7030f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7030f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7030f-105">Define una [estructura ADRLIST](adrlist.md) con el nombre especificado que contiene un número especificado de estructuras [ADRENTRY.](adrentry.md)</span><span class="sxs-lookup"><span data-stu-id="7030f-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7030f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7030f-106">Header file:</span></span>  <br/> |<span data-ttu-id="7030f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7030f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7030f-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="7030f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="7030f-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="7030f-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="7030f-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="7030f-110">Parameters</span></span>

<span data-ttu-id="7030f-111">_ _centries_</span><span class="sxs-lookup"><span data-stu-id="7030f-111">_ _centries_</span></span>
  
> <span data-ttu-id="7030f-112">Recuento de **estructuras ADRENTRY** que se incluirán en la nueva **estructura ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="7030f-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="7030f-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="7030f-113">_ _name_</span></span>
  
> <span data-ttu-id="7030f-114">Nombre de la nueva **estructura ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="7030f-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7030f-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7030f-115">Remarks</span></span>

<span data-ttu-id="7030f-116">La **macro SizedADRLIST** permite definir una lista de destinatarios que tiene límites explícitos cuando se conocen los requisitos de longitud de la matriz.</span><span class="sxs-lookup"><span data-stu-id="7030f-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="7030f-117">El código siguiente muestra cómo convertir el resultado de la macro **SizedADRLIST** en un **puntero de estructura ADRLIST:**</span><span class="sxs-lookup"><span data-stu-id="7030f-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="7030f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="7030f-118">See also</span></span>

- [<span data-ttu-id="7030f-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="7030f-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="7030f-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="7030f-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="7030f-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="7030f-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

