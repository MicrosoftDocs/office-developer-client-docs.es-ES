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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423016"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="00420-103">Función CALLOUTTARGETREF</span><span class="sxs-lookup"><span data-stu-id="00420-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="00420-104">Devuelve una referencia de hoja a la forma de destino de la forma de llamada.</span><span class="sxs-lookup"><span data-stu-id="00420-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="00420-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="00420-105">Version Information</span></span>

<span data-ttu-id="00420-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="00420-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="00420-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00420-107">Syntax</span></span>

<span data-ttu-id="00420-108">CALLOUTTARGETREF ()!</span><span class="sxs-lookup"><span data-stu-id="00420-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="00420-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00420-109">Return value</span></span>

<span data-ttu-id="00420-110">Referencia de ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="00420-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00420-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00420-111">Remarks</span></span>

<span data-ttu-id="00420-112">Si la forma no es una forma de llamada o si no está asociada a una forma de destino, CALLOUTTARGETREF devuelve #REF.</span><span class="sxs-lookup"><span data-stu-id="00420-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="00420-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="00420-113">Example</span></span>

<span data-ttu-id="00420-114">CALLOUTTARGETREF ()! Alto</span><span class="sxs-lookup"><span data-stu-id="00420-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="00420-115">Devuelve el valor de la celda Height de la forma que está asociada a la llamada.</span><span class="sxs-lookup"><span data-stu-id="00420-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

