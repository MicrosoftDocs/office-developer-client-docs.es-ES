---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- fdance (función) [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7a2fbdf723d06dcf9b02789178d7d12d0515884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815637"
---
# <a name="fdance"></a><span data-ttu-id="812e4-104">fDance</span><span class="sxs-lookup"><span data-stu-id="812e4-104">fDance</span></span>

 <span data-ttu-id="812e4-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="812e4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="812e4-106">Comando de ejemplo definida por el usuario que cambia las celdas seleccionadas en la hoja de cálculo activa alrededor hasta que el usuario presiona la **tecla ESC**.</span><span class="sxs-lookup"><span data-stu-id="812e4-106">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**.</span></span> <span data-ttu-id="812e4-107">Cuando se carga GENERIC.xll, crea un menú definido por el usuario, genérico, a través del cual se obtiene acceso a este comando.</span><span class="sxs-lookup"><span data-stu-id="812e4-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="812e4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="812e4-108">Parameters</span></span>

<span data-ttu-id="812e4-109">La función no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="812e4-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="812e4-110">Propiedad valor y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="812e4-110">Property value/Return value</span></span>

<span data-ttu-id="812e4-111">La función siempre devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="812e4-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="812e4-112">Notas</span><span class="sxs-lookup"><span data-stu-id="812e4-112">Remarks</span></span>

<span data-ttu-id="812e4-113">Éste es un ejemplo de una operación larga.</span><span class="sxs-lookup"><span data-stu-id="812e4-113">This is an example of a lengthy operation.</span></span> <span data-ttu-id="812e4-114">Llama a la función [xlAbort](xlabort.md) ocasionalmente.</span><span class="sxs-lookup"><span data-stu-id="812e4-114">It calls the function [xlAbort](xlabort.md) occasionally.</span></span> <span data-ttu-id="812e4-115">Esto da como resultado el procesador (ayudar con tareas cooperación) y comprueba si el usuario ha presionado la **tecla ESC** para cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="812e4-115">This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation.</span></span> <span data-ttu-id="812e4-116">Si es así, ofrece al usuario una oportunidad para cancelar la anulación.</span><span class="sxs-lookup"><span data-stu-id="812e4-116">If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="812e4-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="812e4-117">Example</span></span>

<span data-ttu-id="812e4-118">Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función.</span><span class="sxs-lookup"><span data-stu-id="812e4-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="812e4-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="812e4-119">See also</span></span>



[<span data-ttu-id="812e4-120">Funciones en el archivo DLL genérica</span><span class="sxs-lookup"><span data-stu-id="812e4-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

