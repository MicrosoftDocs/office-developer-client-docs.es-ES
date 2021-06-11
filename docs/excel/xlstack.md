---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- función xlstack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429982"
---
# <a name="xlstack"></a><span data-ttu-id="b1b01-104">xlStack</span><span class="sxs-lookup"><span data-stu-id="b1b01-104">xlStack</span></span>

<span data-ttu-id="b1b01-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b1b01-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b1b01-106">Comprueba la cantidad de espacio que queda en la pila.</span><span class="sxs-lookup"><span data-stu-id="b1b01-106">Checks the amount of space left on the stack.</span></span>
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="b1b01-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1b01-107">Parameters</span></span>

<span data-ttu-id="b1b01-108">Esta función no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="b1b01-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b1b01-109">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1b01-109">Property value/Return value</span></span>

<span data-ttu-id="b1b01-110">Devuelve el número de bytes (**xltypeInt**) restantes en la pila.</span><span class="sxs-lookup"><span data-stu-id="b1b01-110">Returns the number of bytes (**xltypeInt**) remaining on the stack.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1b01-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1b01-111">Remarks</span></span>

<span data-ttu-id="b1b01-112">La cantidad de espacio de pila disponible de las versiones recientes desborda el entero con signo de 16 bits del **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="b1b01-112">The amount of available stack space of recent versions overflows the 16-bit signed integer of the **XLOPER**.</span></span> <span data-ttu-id="b1b01-113">Esto significa que **xlStack** puede devolver un valor entre -32767 y 32768 cuando se llama con **XLOPER** s y **Excel4** o **Excel4v**.</span><span class="sxs-lookup"><span data-stu-id="b1b01-113">This means that **xlStack** can return a value between -32767 and 32768 when called using **XLOPER** s and **Excel4** or **Excel4v**.</span></span> <span data-ttu-id="b1b01-114">Para obtener el valor correcto en este caso, debe convertir el valor devuelto en un short sin signo.</span><span class="sxs-lookup"><span data-stu-id="b1b01-114">To obtain the correct value in this case, you must cast the returned value to an unsigned short.</span></span>
  
<span data-ttu-id="b1b01-115">A partir de Excel 2007, debe llamar a esta función con **XLOPER12** s y **Excel12** o **Excel12v**, en cuyo caso el valor devuelto es la cantidad de espacio de pila disponible o 64 KB, lo que sea menor.</span><span class="sxs-lookup"><span data-stu-id="b1b01-115">Starting in Excel 2007, you should call this function using **XLOPER12** s and **Excel12** or **Excel12v**, in which case the returned value is amount of stack space available or 64 KB, whichever is the lesser.</span></span>
  
<span data-ttu-id="b1b01-116">Excel tiene una cantidad limitada de espacio en la pila y debe tener cuidado de no saturar este espacio.</span><span class="sxs-lookup"><span data-stu-id="b1b01-116">Excel has a limited amount of space on the stack, and you should take care not to overrun this space.</span></span> <span data-ttu-id="b1b01-117">Nunca coloque estructuras de datos muy grandes en la pila y haga que tantas variables locales como sea posible estáticas.</span><span class="sxs-lookup"><span data-stu-id="b1b01-117">Never put very large data structures on the stack, and make as many local variables as possible static.</span></span> <span data-ttu-id="b1b01-118">Evite llamar a funciones de forma recursiva, porque eso rellenará rápidamente la pila.</span><span class="sxs-lookup"><span data-stu-id="b1b01-118">Avoid calling functions recursively, because that will quickly fill up the stack.</span></span>
  
<span data-ttu-id="b1b01-119">Si sospecha que está rebando la pila, llame a esta función con frecuencia para ver cuánto espacio de pila queda.</span><span class="sxs-lookup"><span data-stu-id="b1b01-119">If you suspect that you are overrunning the stack, call this function frequently to see how much stack space is left.</span></span>
  
## <a name="example"></a><span data-ttu-id="b1b01-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1b01-120">Example</span></span>

<span data-ttu-id="b1b01-121">El primer ejemplo muestra un mensaje de alerta que contiene la cantidad de espacio de pila que queda y se encuentra en  `\SAMPLES\EXAMPLE\EXAMPLE.C` .</span><span class="sxs-lookup"><span data-stu-id="b1b01-121">The first example displays an alert message containing the amount of stack space left and is contained in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="b1b01-122">El segundo ejemplo hace lo mismo, trabajando con **XLOPER** s y no está contenido en el código de ejemplo del SDK.</span><span class="sxs-lookup"><span data-stu-id="b1b01-122">The second example does the same thing, working with **XLOPER** s and is not contained in the SDK example code.</span></span>
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="b1b01-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1b01-123">See also</span></span>

- [<span data-ttu-id="b1b01-124">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="b1b01-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

