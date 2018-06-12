---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- función xlCoerce [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0474b81a6d24663fe85303efc8fe2fd62cfdd82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815730"
---
# <a name="xlcoerce"></a><span data-ttu-id="37fcf-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="37fcf-104">xlCoerce</span></span>

 <span data-ttu-id="37fcf-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="37fcf-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="37fcf-106">Convierte un tipo de **XLOPER**/ **XLOPER12** a otro, o tiene el mismo aspecto los valores de celda en una hoja.</span><span class="sxs-lookup"><span data-stu-id="37fcf-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="37fcf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37fcf-107">Parameters</span></span>

 <span data-ttu-id="37fcf-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="37fcf-108">_pxSource_</span></span>
  
<span data-ttu-id="37fcf-109">El origen de **XLOPER**/ **XLOPER12** que necesita que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="37fcf-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="37fcf-110">_pxDestType_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="37fcf-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="37fcf-111">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="37fcf-111">(Optional).</span></span> <span data-ttu-id="37fcf-112">Una máscara de bits de los tipos resultantes están dispuestos a Aceptar.</span><span class="sxs-lookup"><span data-stu-id="37fcf-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="37fcf-113">Debe usar el operador **OR** bit a bit (|) para especificar varios tipos posibles.</span><span class="sxs-lookup"><span data-stu-id="37fcf-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="37fcf-114">Si se omite este argumento, las referencias a celdas individuales se convierten en uno de los tipos de valor **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (si la celda a que se refiere a está vacía) y las referencias a los bloques de las celdas se convierten en **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="37fcf-114">If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**.</span></span> <span data-ttu-id="37fcf-115">Esto hace que **xlCoerce** la forma más conveniente para buscar valores de celda.</span><span class="sxs-lookup"><span data-stu-id="37fcf-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="37fcf-116">Propiedad valor y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37fcf-116">Property value/Return value</span></span>

<span data-ttu-id="37fcf-117">Devuelve el valor convertido (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**o **xltypeMulti**).</span><span class="sxs-lookup"><span data-stu-id="37fcf-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37fcf-118">Notas</span><span class="sxs-lookup"><span data-stu-id="37fcf-118">Remarks</span></span>

 <span data-ttu-id="37fcf-119">no se puede convertir **xlCoerce** a o desde **xltypeBigData** o **xltypeFlow**.</span><span class="sxs-lookup"><span data-stu-id="37fcf-119">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**.</span></span> <span data-ttu-id="37fcf-120">Pasar un tipo de **xltypeMissing** o **xltypeNil** como _pxDestType_ es equivalente a si se omite el argumento.</span><span class="sxs-lookup"><span data-stu-id="37fcf-120">Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument.</span></span> <span data-ttu-id="37fcf-121">Puede producirse un error de conversión en algunos casos.</span><span class="sxs-lookup"><span data-stu-id="37fcf-121">Conversion can fail in some cases.</span></span> <span data-ttu-id="37fcf-122">Por ejemplo, algunas cadenas no se puede convertir a números, mientras que otros usuarios puedan.</span><span class="sxs-lookup"><span data-stu-id="37fcf-122">For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="37fcf-123">Si una matriz o una referencia de celda múltiples se convierte en un tipo de valor único, el resultado es el valor de la superior izquierdo celda o elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="37fcf-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="37fcf-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37fcf-124">Example</span></span>

<span data-ttu-id="37fcf-125">El siguiente código puede encontrarse en `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="37fcf-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="37fcf-126">La función **xlcAlert** implícitamente intenta convertir su argumento en una cadena de modo que en realidad se pudo quitar el paso de conversión que se muestra aquí y **xInt** se podía pasar directamente a **xlcAlert**.</span><span class="sxs-lookup"><span data-stu-id="37fcf-126">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**.</span></span> <span data-ttu-id="37fcf-127">Como **xlcAlert** es una macro de comando, este código sólo funciona correctamente cuando se llame desde una hoja de macros.</span><span class="sxs-lookup"><span data-stu-id="37fcf-127">As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="37fcf-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="37fcf-128">See also</span></span>



[<span data-ttu-id="37fcf-129">xlSet</span><span class="sxs-lookup"><span data-stu-id="37fcf-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="37fcf-130">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="37fcf-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

