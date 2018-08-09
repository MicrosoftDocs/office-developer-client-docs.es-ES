---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- xloper12toxloper (función) [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815747"
---
# <a name="xloper12toxloper"></a><span data-ttu-id="9c05e-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="9c05e-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="9c05e-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9c05e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9c05e-106">Rutina de conversión que se usa para convertir de nuevo **XLOPER12** a la antigua **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="9c05e-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="9c05e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c05e-107">Parameters</span></span>

<span data-ttu-id="9c05e-108">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="9c05e-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="9c05e-109">Puntero al origen de **XLOPER12** que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="9c05e-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="9c05e-110">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="9c05e-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="9c05e-111">Puntero al destino **XLOPER** para contener el valor convertido.</span><span class="sxs-lookup"><span data-stu-id="9c05e-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9c05e-112">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c05e-112">Property value/Return value</span></span>

<span data-ttu-id="9c05e-113">**TRUE** si la conversión se ha realizado correctamente, **FALSE** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9c05e-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9c05e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9c05e-114">Remarks</span></span>

<span data-ttu-id="9c05e-115">Según el tipo de **XLOPER12**, esta función asigna un nuevo búfer de memoria para los valores convertidos, que se hace referencia en el destino **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="9c05e-115">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**.</span></span> <span data-ttu-id="9c05e-116">El autor de la llamada es responsable de liberar cualquier memoria asociada con la copia si la conversión es un éxito; Se puede usar **FreeXLOperT** , o se puede realizar directamente mediante el uso de **libre**.</span><span class="sxs-lookup"><span data-stu-id="9c05e-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="9c05e-117">Si se produce un error en la conversión, el autor de la llamada no necesita liberar cualquier memoria.</span><span class="sxs-lookup"><span data-stu-id="9c05e-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="9c05e-118">Puede producirse un error en la conversión de un **XLOPER12** a un **XLOPER** cuando **XLOPER12** contiene una matriz o referencia que es demasiado grande o una cadena que es demasiado larga para el **XLOPER** contener.</span><span class="sxs-lookup"><span data-stu-id="9c05e-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="9c05e-119">**XLOPER12** Cadenas de caracteres anchos de Unicode se convierten en cadenas de bytes **XLOPER** ASCII en un modo que sea configuración regional-dependiente.</span><span class="sxs-lookup"><span data-stu-id="9c05e-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="9c05e-120">El **XLOPER12** **xltypeInt** es un entero con signo de 32 bits, mientras que el **XLOPER** **xltypeInt** es un entero con signo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="9c05e-120">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer.</span></span> <span data-ttu-id="9c05e-121">Cuando un entero **XLOPER12** proporcionado supera el límite de entero **XLOPER** , el número entero se convierte en un doble de 8 bytes y se devuelven en un **XLOPER** de tipo **xltypeNum**.</span><span class="sxs-lookup"><span data-stu-id="9c05e-121">When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**.</span></span> <span data-ttu-id="9c05e-122">Esto es el único caso en que esta función cambia el tipo de la convertida **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="9c05e-122">This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="9c05e-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9c05e-123">Example</span></span>

<span data-ttu-id="9c05e-124">Consulte el archivo `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para el código para esta función.</span><span class="sxs-lookup"><span data-stu-id="9c05e-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9c05e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c05e-125">See also</span></span>

- [<span data-ttu-id="9c05e-126">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="9c05e-126">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

