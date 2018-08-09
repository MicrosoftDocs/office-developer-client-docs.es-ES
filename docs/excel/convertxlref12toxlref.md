---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- convertxlref12toxlref (función) [excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 826428edb57eba9e17d601164aa8b4b797fc8929
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815524"
---
# <a name="convertxlref12toxlref"></a><span data-ttu-id="aab3f-104">ConvertXLRef12ToXLRef</span><span class="sxs-lookup"><span data-stu-id="aab3f-104">ConvertXLRef12ToXLRef</span></span>

<span data-ttu-id="aab3f-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="aab3f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="aab3f-106">Intenta convertir un **XLREF12** en un **XLREF**.</span><span class="sxs-lookup"><span data-stu-id="aab3f-106">Tries to convert an **XLREF12** into an **XLREF**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a><span data-ttu-id="aab3f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aab3f-107">Parameters</span></span>

 <span data-ttu-id="aab3f-108">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="aab3f-108">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="aab3f-109">Puntero a la estructura del origen de referencia.</span><span class="sxs-lookup"><span data-stu-id="aab3f-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="aab3f-110">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="aab3f-110">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="aab3f-111">Puntero a la estructura de referencia de destino en el que el valor convertido es que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="aab3f-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="aab3f-112">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aab3f-112">Property value/Return value</span></span>

 <span data-ttu-id="aab3f-113">**TRUE** si la conversión se ha realizado correctamente, **FALSE** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="aab3f-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="aab3f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aab3f-114">Remarks</span></span>

<span data-ttu-id="aab3f-115">Se produce un error en la conversión de **XLREF12** a **XLREF** si la referencia proporcionada hace referencia a la parte de una hoja de cálculo de Excel 2007 que no es compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="aab3f-115">The conversion from **XLREF12** to **XLREF** fails if the supplied reference refers to part of a Excel 2007 worksheet that is not supported in earlier versions.</span></span> 
  
## <a name="example"></a><span data-ttu-id="aab3f-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aab3f-116">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="aab3f-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="aab3f-117">See also</span></span>



[<span data-ttu-id="aab3f-118">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="aab3f-118">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

