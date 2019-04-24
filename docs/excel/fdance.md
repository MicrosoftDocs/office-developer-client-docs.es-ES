---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- función fdance [Excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311042"
---
# <a name="fdance"></a><span data-ttu-id="613d5-104">fDance</span><span class="sxs-lookup"><span data-stu-id="613d5-104">fDance</span></span>

 <span data-ttu-id="613d5-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="613d5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="613d5-106">Comando definido por el usuario de ejemplo que cambia las celdas seleccionadas en la hoja de cálculo activa hasta que el usuario presiona la **tecla ESC**.</span><span class="sxs-lookup"><span data-stu-id="613d5-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="613d5-107">Cuando se carga GENERIC. XLL, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando.</span><span class="sxs-lookup"><span data-stu-id="613d5-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="613d5-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="613d5-108">Parameters</span></span>

<span data-ttu-id="613d5-109">La función no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="613d5-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="613d5-110">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="613d5-110">Property value/Return value</span></span>

<span data-ttu-id="613d5-111">La función siempre devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="613d5-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="613d5-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="613d5-112">Remarks</span></span>

<span data-ttu-id="613d5-113">Este es un ejemplo de una operación larga.</span><span class="sxs-lookup"><span data-stu-id="613d5-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="613d5-114">Llama a la función [xlAbort](xlabort.md) de vez en cuando.</span><span class="sxs-lookup"><span data-stu-id="613d5-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="613d5-115">Esto produce el procesador (ayudando con la multitarea cooperativa) y comprueba si el usuario ha presionado **ESC** para cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="613d5-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="613d5-116">Si es así, ofrece al usuario la posibilidad de cancelar la anulación.</span><span class="sxs-lookup"><span data-stu-id="613d5-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="613d5-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="613d5-117">Example</span></span>

<span data-ttu-id="613d5-118">Consulte `\SAMPLES\GENERIC\GENERIC.C` para obtener el código fuente de esta función.</span><span class="sxs-lookup"><span data-stu-id="613d5-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="613d5-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="613d5-119">See also</span></span>



[<span data-ttu-id="613d5-120">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="613d5-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

