---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- función convertxlreftoxlref12 [Excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 530cb9cce5b0023318ff6b8a0ff73472f8250aa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432033"
---
# <a name="convertxlreftoxlref12"></a><span data-ttu-id="70fe6-104">ConvertXLRefToXLRef12</span><span class="sxs-lookup"><span data-stu-id="70fe6-104">ConvertXLRefToXLRef12</span></span>

<span data-ttu-id="70fe6-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="70fe6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="70fe6-106">Función de Framework que intenta convertir un **XLREF** en un **XLREF12**.</span><span class="sxs-lookup"><span data-stu-id="70fe6-106">Framework function that attempts to convert an **XLREF** into an **XLREF12**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a><span data-ttu-id="70fe6-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="70fe6-107">Parameters</span></span>

 <span data-ttu-id="70fe6-108">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="70fe6-108">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="70fe6-109">Puntero a la estructura de referencia de origen.</span><span class="sxs-lookup"><span data-stu-id="70fe6-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="70fe6-110">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="70fe6-110">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="70fe6-111">Puntero a la estructura de referencia de destino en la que se va a colocar el valor convertido.</span><span class="sxs-lookup"><span data-stu-id="70fe6-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="70fe6-112">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70fe6-112">Property value/Return value</span></span>

 <span data-ttu-id="70fe6-113">**True** si la conversión se realizó correctamente; de lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="70fe6-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="70fe6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="70fe6-114">Remarks</span></span>

<span data-ttu-id="70fe6-115">Siempre que el **XLREF** pasado sea válido, esta operación siempre debe realizarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="70fe6-115">Provided that the passed-in **XLREF** is valid, this operation should always be successful.</span></span> <span data-ttu-id="70fe6-116">Por el contrario, la conversión de la otra forma de **XLREF12** a **XLREF**, realizada por [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), produce un error si la referencia proporcionada hace referencia a parte de una hoja de cálculo de Excel 2007 que no es compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="70fe6-116">In contrast, conversion the other way from **XLREF12** to **XLREF**, performed by [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), fails if the supplied reference refers to part of an Excel 2007 worksheet that is not supported in earlier versions.</span></span>
  
## <a name="example"></a><span data-ttu-id="70fe6-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70fe6-117">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="70fe6-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="70fe6-118">See also</span></span>



[<span data-ttu-id="70fe6-119">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="70fe6-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

