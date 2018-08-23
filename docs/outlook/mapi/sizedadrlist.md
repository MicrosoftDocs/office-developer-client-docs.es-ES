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
ms.openlocfilehash: 62911e0dec15002f39fff81e8c517c1cb11d0183
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574744"
---
# <a name="sizedadrlist"></a><span data-ttu-id="218a1-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="218a1-103">SizedADRLIST</span></span>

<span data-ttu-id="218a1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="218a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="218a1-105">Define una estructura de [ADRLIST](adrlist.md) con el nombre especificado que contiene un número especificado de estructuras [ADRENTRY](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="218a1-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="218a1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="218a1-106">Header file:</span></span>  <br/> |<span data-ttu-id="218a1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="218a1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="218a1-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="218a1-108">Related structure:</span></span>  <br/> |<span data-ttu-id="218a1-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="218a1-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="218a1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="218a1-110">Parameters</span></span>

<span data-ttu-id="218a1-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="218a1-111">__centries_</span></span>
  
> <span data-ttu-id="218a1-112">Recuento de las estructuras **ADRENTRY** que se deben incluir en la nueva estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="218a1-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="218a1-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="218a1-113">__name_</span></span>
  
> <span data-ttu-id="218a1-114">Nombre de la nueva estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="218a1-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="218a1-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="218a1-115">Remarks</span></span>

<span data-ttu-id="218a1-116">La macro **SizedADRLIST** le permite definir una lista de destinatarios que tiene límites explícitos cuando se conocen los requisitos de longitud de la matriz.</span><span class="sxs-lookup"><span data-stu-id="218a1-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="218a1-117">El código siguiente muestra cómo convertir el resultado de la macro **SizedADRLIST** a un puntero de estructura **ADRLIST** :</span><span class="sxs-lookup"><span data-stu-id="218a1-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="218a1-118">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="218a1-118">See also</span></span>

- [<span data-ttu-id="218a1-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="218a1-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="218a1-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="218a1-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="218a1-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="218a1-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

