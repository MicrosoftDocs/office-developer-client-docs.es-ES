---
title: CALLOUTTARGETREF (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Devuelve una referencia de hoja a la forma de destino de la forma de llamada.
ms.openlocfilehash: 1b0cb7c6737a810a0ade65f19afaff7bb4b9f616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821681"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="44e54-103">Función CALLOUTTARGETREF</span><span class="sxs-lookup"><span data-stu-id="44e54-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="44e54-104">Devuelve una referencia de hoja a la forma de destino de la forma de llamada.</span><span class="sxs-lookup"><span data-stu-id="44e54-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="44e54-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="44e54-105">Version Information</span></span>

<span data-ttu-id="44e54-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="44e54-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="44e54-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44e54-107">Syntax</span></span>

<span data-ttu-id="44e54-108">CALLOUTTARGETREF()!</span><span class="sxs-lookup"><span data-stu-id="44e54-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="44e54-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44e54-109">Return value</span></span>

<span data-ttu-id="44e54-110">Referencia de ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="44e54-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44e54-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44e54-111">Remarks</span></span>

<span data-ttu-id="44e54-112">Si la forma no es una forma de llamada, o si no está asociado con una forma de destino, CALLOUTTARGETREF devuelve #REF.</span><span class="sxs-lookup"><span data-stu-id="44e54-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="44e54-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="44e54-113">Example</span></span>

<span data-ttu-id="44e54-114">CALLOUTTARGETREF()!Height</span><span class="sxs-lookup"><span data-stu-id="44e54-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="44e54-115">Devuelve el valor de la celda Height de la forma que está asociada a la llamada.</span><span class="sxs-lookup"><span data-stu-id="44e54-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

