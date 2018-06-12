---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- convertxlreftoxlref12 (función) [excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f2830633482e5329d285907b610386b708c406a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815531"
---
# <a name="convertxlreftoxlref12"></a><span data-ttu-id="b04ff-104">ConvertXLRefToXLRef12</span><span class="sxs-lookup"><span data-stu-id="b04ff-104">ConvertXLRefToXLRef12</span></span>

<span data-ttu-id="b04ff-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b04ff-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b04ff-106">Función de Framework que intenta convertir un **XLREF** en un **XLREF12**.</span><span class="sxs-lookup"><span data-stu-id="b04ff-106">Framework function that attempts to convert an **XLREF** into an **XLREF12**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a><span data-ttu-id="b04ff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b04ff-107">Parameters</span></span>

 <span data-ttu-id="b04ff-108">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="b04ff-108">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="b04ff-109">Puntero a la estructura del origen de referencia.</span><span class="sxs-lookup"><span data-stu-id="b04ff-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="b04ff-110">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="b04ff-110">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="b04ff-111">Puntero a la estructura de referencia de destino en el que el valor convertido es que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="b04ff-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b04ff-112">Propiedad valor y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b04ff-112">Property value/Return value</span></span>

 <span data-ttu-id="b04ff-113">**TRUE** si la conversión se ha realizado correctamente, **FALSE** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b04ff-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b04ff-114">Notas</span><span class="sxs-lookup"><span data-stu-id="b04ff-114">Remarks</span></span>

<span data-ttu-id="b04ff-115">Siempre que se pasan en **XLREF** es válida, esta operación debe ser siempre correcta.</span><span class="sxs-lookup"><span data-stu-id="b04ff-115">Provided that the passed-in **XLREF** is valid, this operation should always be successful.</span></span> <span data-ttu-id="b04ff-116">Por el contrario, conversión de la otra forma de **XLREF12** **XLREF**, realizado por [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), se produce un error si la referencia proporcionada hace referencia a la parte de una hoja de cálculo de Excel 2007 que no es compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="b04ff-116">In contrast, conversion the other way from **XLREF12** to **XLREF**, performed by [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), fails if the supplied reference refers to part of an Excel 2007 worksheet that is not supported in earlier versions.</span></span>
  
## <a name="example"></a><span data-ttu-id="b04ff-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b04ff-117">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxref, LPXLREF12 pxref12)
{
   if (pxref->rwLast >= pxref->rwFirst && pxref->colLast >= pxref->colFirst)
   {
      if (pxref->rwFirst >= 0 && pxref->colFirst >= 0)
      {
         pxref12->rwFirst = pxref->rwFirst;
         pxref12->rwLast = pxref->rwLast;
         pxref12->colFirst = pxref->colFirst;
         pxref12->colLast = pxref->colLast;
         return TRUE;
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="b04ff-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b04ff-118">See also</span></span>



[<span data-ttu-id="b04ff-119">Funciones de la biblioteca de Framework</span><span class="sxs-lookup"><span data-stu-id="b04ff-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

