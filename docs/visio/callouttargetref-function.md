---
title: CALLOUTTARGETREF (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Devuelve una referencia de hoja a la forma de destino de la forma de llamada.
ms.openlocfilehash: aeeb919fb2efc175d8e5ce23f464503c13331249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337250"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="67612-103">Función CALLOUTTARGETREF</span><span class="sxs-lookup"><span data-stu-id="67612-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="67612-104">Devuelve una referencia de hoja a la forma de destino de la forma de llamada.</span><span class="sxs-lookup"><span data-stu-id="67612-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="67612-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="67612-105">Version Information</span></span>

<span data-ttu-id="67612-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="67612-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="67612-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67612-107">Syntax</span></span>

<span data-ttu-id="67612-108">CALLOUTTARGETREF ()!</span><span class="sxs-lookup"><span data-stu-id="67612-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="67612-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67612-109">Return value</span></span>

<span data-ttu-id="67612-110">Referencia de ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="67612-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67612-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="67612-111">Remarks</span></span>

<span data-ttu-id="67612-112">Si la forma no es una forma de llamada o si no está asociada a una forma de destino, CALLOUTTARGETREF devuelve #REF.</span><span class="sxs-lookup"><span data-stu-id="67612-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="67612-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="67612-113">Example</span></span>

<span data-ttu-id="67612-114">CALLOUTTARGETREF ()! Alto</span><span class="sxs-lookup"><span data-stu-id="67612-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="67612-115">Devuelve el valor de la celda Height de la forma que está asociada a la llamada.</span><span class="sxs-lookup"><span data-stu-id="67612-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

