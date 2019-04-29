---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- función xlgethwnd [Excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425459"
---
# <a name="xlgethwnd"></a><span data-ttu-id="58b77-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="58b77-104">xlGetHwnd</span></span>

<span data-ttu-id="58b77-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="58b77-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="58b77-106">Devuelve el controlador de la ventana de Microsoft Excel de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="58b77-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="58b77-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="58b77-107">Parameters</span></span>

<span data-ttu-id="58b77-108">Esta función no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="58b77-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="58b77-109">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58b77-109">Property value/Return value</span></span>

<span data-ttu-id="58b77-110">Contiene el identificador de ventana (**xltypeInt**) en el campo **Val. w** .</span><span class="sxs-lookup"><span data-stu-id="58b77-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="58b77-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58b77-111">Remarks</span></span>

<span data-ttu-id="58b77-112">Esta función es útil para escribir código de API de Windows.</span><span class="sxs-lookup"><span data-stu-id="58b77-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="58b77-113">Cuando se llama a esta función mediante [Excel4](excel4-excel12.md) o [Excel4v](excel4v-excel12v.md), la variable de entero del XLOPER que se devuelve es un int Short de 16 bits firmado. Esto solo puede contener los 16 bits bajos del controlador de Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="58b77-113">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="58b77-114">Para encontrar la parte alta, el código debe recorrer en iteración todas las ventanas abiertas que busquen una coincidencia con la parte baja.</span><span class="sxs-lookup"><span data-stu-id="58b77-114">To find the high part, your code must iterate through all open windows looking for a match with the low part.</span></span> <span data-ttu-id="58b77-115">A partir de Excel 2007, la variable de entero de **XLOPER12** es un int de 32 bits firmado y, por lo tanto, contiene todo el identificador, lo que elimina la necesidad de recorrer en iteración todas las ventanas abiertas.</span><span class="sxs-lookup"><span data-stu-id="58b77-115">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="58b77-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58b77-116">Example</span></span>

<span data-ttu-id="58b77-117">Consulte el código de la [función fShowDialog](fshowdialog.md) en `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="58b77-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="58b77-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="58b77-118">See also</span></span>

- [<span data-ttu-id="58b77-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="58b77-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="58b77-120">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="58b77-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

