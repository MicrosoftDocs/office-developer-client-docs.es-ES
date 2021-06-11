---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- Función xloper12toxloper [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 148353dcec1cc051aa44d18c0a081b6623e3759a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422911"
---
# <a name="xloper12toxloper"></a><span data-ttu-id="54eac-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="54eac-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="54eac-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="54eac-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="54eac-106">Rutina de conversión usada para convertir del **nuevo XLOPER12** al **XLOPER antiguo**.</span><span class="sxs-lookup"><span data-stu-id="54eac-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="54eac-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="54eac-107">Parameters</span></span>

<span data-ttu-id="54eac-108">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="54eac-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="54eac-109">Puntero al **origen XLOPER12** que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="54eac-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="54eac-110">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="54eac-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="54eac-111">Puntero al **XLOPER de destino** para contener el valor convertido.</span><span class="sxs-lookup"><span data-stu-id="54eac-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="54eac-112">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54eac-112">Property value/Return value</span></span>

<span data-ttu-id="54eac-113">**TRUE** si la conversión se ha hecho correctamente, **FALSE** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="54eac-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="54eac-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54eac-114">Remarks</span></span>

<span data-ttu-id="54eac-115">Según el tipo de **XLOPER12**, esta función asigna un nuevo búfer de memoria para los valores convertidos, que se apuntan en el **XLOPER de** destino.</span><span class="sxs-lookup"><span data-stu-id="54eac-115">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**.</span></span> <span data-ttu-id="54eac-116">El autor de la llamada es responsable de liberar cualquier memoria asociada a la copia si la conversión es correcta; **FreeXLOperT** puede usarse o puede hacerse directamente mediante **el uso** gratuito de .</span><span class="sxs-lookup"><span data-stu-id="54eac-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="54eac-117">Si se produce un error en la conversión, el autor de la llamada no necesita liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="54eac-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="54eac-118">La conversión de **un XLOPER12** a **un XLOPER** puede producir un error cuando **XLOPER12** contiene una matriz o referencia demasiado grande o una cadena demasiado larga para que **XLOPER** contenga.</span><span class="sxs-lookup"><span data-stu-id="54eac-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="54eac-119">**XLOPER12** Las cadenas de caracteres anchos Unicode se convierten en cadenas de bytes ASCII **XLOPER** de una forma que depende de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="54eac-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="54eac-120">**XLOPER12** **xltypeInt** es un entero con signo de 32 bits, mientras que **XLOPER** **xltypeInt** es un entero con signo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="54eac-120">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer.</span></span> <span data-ttu-id="54eac-121">Cuando un entero **XLOPER12** proporcionado supera el límite de un entero **XLOPER,** el entero se convierte en un doble de 8 bytes y se devuelve en un **XLOPER** de tipo **xltypeNum**.</span><span class="sxs-lookup"><span data-stu-id="54eac-121">When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**.</span></span> <span data-ttu-id="54eac-122">Este es el único caso en el que esta función cambia el tipo de **XLOPER convertido.**</span><span class="sxs-lookup"><span data-stu-id="54eac-122">This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="54eac-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54eac-123">Example</span></span>

<span data-ttu-id="54eac-124">Vea el archivo  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para obtener el código de esta función.</span><span class="sxs-lookup"><span data-stu-id="54eac-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54eac-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="54eac-125">See also</span></span>

- [<span data-ttu-id="54eac-126">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="54eac-126">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

