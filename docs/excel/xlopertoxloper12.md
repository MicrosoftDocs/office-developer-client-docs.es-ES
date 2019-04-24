---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- función xlopertoxloper12 [Excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303909"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="368d7-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="368d7-104">XLOperToXLOper12</span></span>

<span data-ttu-id="368d7-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="368d7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="368d7-106">Rutina de conversión que se usa para convertir del **XLOPER** antiguo al nuevo **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="368d7-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="368d7-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="368d7-107">Parameters</span></span>

<span data-ttu-id="368d7-108">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="368d7-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="368d7-109">Puntero al **XLOPER** de origen que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="368d7-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="368d7-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="368d7-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="368d7-111">Puntero al **XLOPER12** de destino para que contenga el valor convertido.</span><span class="sxs-lookup"><span data-stu-id="368d7-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="368d7-112">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="368d7-112">Property value/Return value</span></span>

<span data-ttu-id="368d7-113">**True** si la conversión se realizó correctamente; de lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="368d7-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="368d7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="368d7-114">Remarks</span></span>

<span data-ttu-id="368d7-115">Según el tipo de **XLOPER**, esta función asigna un nuevo búfer de memoria para los valores convertidos, que se señalan en el **XLOPER12**de destino.</span><span class="sxs-lookup"><span data-stu-id="368d7-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="368d7-116">El autor de la llamada es responsable de liberar cualquier memoria asociada a la copia si la conversión es un éxito; Se puede usar **FreeXLOper12T** , o bien se puede hacer directamente con **Free**.</span><span class="sxs-lookup"><span data-stu-id="368d7-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="368d7-117">Si se produce un error en la conversión, el autor de la llamada no necesita liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="368d7-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="368d7-118">En general, es posible convertir de cualquier **XLOPER** a **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="368d7-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="368d7-119">Por el contrario, se puede producir un error en la conversión de un **XLOPER12** a un **XLOPER** cuando el **XLOPER12** contiene una matriz o referencia demasiado grande o una cadena demasiado larga para que **XLOPER** la contenga.</span><span class="sxs-lookup"><span data-stu-id="368d7-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="368d7-120">**XLOPER** Las cadenas de bytes ASCII se convierten en las cadenas de caracteres anchos Unicode de **XLOPER12** de forma que dependen de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="368d7-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="368d7-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="368d7-121">Example</span></span>

<span data-ttu-id="368d7-122">Vea el archivo `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para obtener el código de esta función.</span><span class="sxs-lookup"><span data-stu-id="368d7-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

