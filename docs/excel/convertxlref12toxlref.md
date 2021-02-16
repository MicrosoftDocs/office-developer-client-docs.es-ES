---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- función convertxlref12toxlref [excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0a12052a93d030088feb548449955129ff5bdc0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432656"
---
# <a name="convertxlref12toxlref"></a><span data-ttu-id="8a934-104">ConvertXLRef12ToXLRef</span><span class="sxs-lookup"><span data-stu-id="8a934-104">ConvertXLRef12ToXLRef</span></span>

<span data-ttu-id="8a934-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8a934-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8a934-106">Intenta convertir un **XLREF12** en **un XLREF**.</span><span class="sxs-lookup"><span data-stu-id="8a934-106">Tries to convert an **XLREF12** into an **XLREF**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a><span data-ttu-id="8a934-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a934-107">Parameters</span></span>

 <span data-ttu-id="8a934-108">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="8a934-108">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="8a934-109">Puntero a la estructura de referencia de origen.</span><span class="sxs-lookup"><span data-stu-id="8a934-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="8a934-110">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="8a934-110">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="8a934-111">Puntero a la estructura de referencia de destino en la que se va a colocar el valor convertido.</span><span class="sxs-lookup"><span data-stu-id="8a934-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="8a934-112">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a934-112">Property value/Return value</span></span>

 <span data-ttu-id="8a934-113">**TRUE** si la conversión se ha hecho correctamente, **FALSE en** caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8a934-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8a934-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8a934-114">Remarks</span></span>

<span data-ttu-id="8a934-115">La conversión de **XLREF12** a **XLREF** produce un error si la referencia proporcionada hace referencia a parte de una hoja de cálculo de Excel 2007 que no es compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="8a934-115">The conversion from **XLREF12** to **XLREF** fails if the supplied reference refers to part of a Excel 2007 worksheet that is not supported in earlier versions.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8a934-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a934-116">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRef12ToXLRef(LPXLREF12 pxref12, LPXLREF pxref)
{
   if (pxref12->rwLast >= pxref12->rwFirst && pxref12->colLast >= pxref12->colFirst)
   {
      if (pxref12->rwFirst >=0 && pxref12->colFirst >= 0)
      {
         if (pxref12->rwLast < rwMaxO8 && pxref12->colLast < colMaxO8)
         {
            pxref->rwFirst = (WORD)pxref12->rwFirst;
            pxref->rwLast = (WORD)pxref12->rwLast;
            pxref->colFirst = (BYTE)pxref12->colFirst;
            pxref->colLast = (BYTE)pxref12->colLast;
            return TRUE;
         }
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="8a934-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a934-117">See also</span></span>



[<span data-ttu-id="8a934-118">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="8a934-118">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

