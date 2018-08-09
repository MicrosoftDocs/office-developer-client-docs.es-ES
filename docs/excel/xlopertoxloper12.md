---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- xlopertoxloper12 (función) [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815762"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="4f3d7-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="4f3d7-104">XLOperToXLOper12</span></span>

<span data-ttu-id="4f3d7-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4f3d7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4f3d7-106">Rutina de conversión que se usa para convertir de la antigua **XLOPER** a la nueva **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="4f3d7-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="4f3d7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f3d7-107">Parameters</span></span>

<span data-ttu-id="4f3d7-108">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="4f3d7-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="4f3d7-109">Puntero al origen de **XLOPER** que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="4f3d7-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="4f3d7-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="4f3d7-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="4f3d7-111">Puntero al destino **XLOPER12** para contener el valor convertido.</span><span class="sxs-lookup"><span data-stu-id="4f3d7-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4f3d7-112">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f3d7-112">Property value/Return value</span></span>

<span data-ttu-id="4f3d7-113">**TRUE** si la conversión se ha realizado correctamente, **FALSE** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4f3d7-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4f3d7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f3d7-114">Remarks</span></span>

<span data-ttu-id="4f3d7-115">Según el tipo de la **XLOPER**, esta función asigna un nuevo búfer de memoria para los valores convertidos, que se hace referencia en el destino **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="4f3d7-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="4f3d7-116">El autor de la llamada es responsable de liberar cualquier memoria asociada con la copia si la conversión es un éxito; Se puede usar **FreeXLOper12T** , o puede realizarse directamente con **gratuita**.</span><span class="sxs-lookup"><span data-stu-id="4f3d7-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="4f3d7-117">Si se produce un error en la conversión, el autor de la llamada no necesita liberar cualquier memoria.</span><span class="sxs-lookup"><span data-stu-id="4f3d7-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="4f3d7-118">En general, la conversión de cualquier **XLOPER** a un **XLOPER12** es posible.</span><span class="sxs-lookup"><span data-stu-id="4f3d7-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="4f3d7-119">Por el contrario, la conversión de un **XLOPER12** un **XLOPER** puede producirse un error cuando el **XLOPER12** contiene una matriz o referencia que es demasiado grande o una cadena que es demasiado larga para el **XLOPER** contener.</span><span class="sxs-lookup"><span data-stu-id="4f3d7-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="4f3d7-120">**XLOPER** Cadenas de bytes ASCII se convierten en cadenas de caracteres anchos de Unicode **XLOPER12** de una manera que depende de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="4f3d7-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="4f3d7-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f3d7-121">Example</span></span>

<span data-ttu-id="4f3d7-122">Consulte el archivo `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para el código para esta función.</span><span class="sxs-lookup"><span data-stu-id="4f3d7-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

