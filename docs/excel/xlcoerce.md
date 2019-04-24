---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- función xlcoerce [Excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303965"
---
# <a name="xlcoerce"></a><span data-ttu-id="cfcaa-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="cfcaa-104">xlCoerce</span></span>

 <span data-ttu-id="cfcaa-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cfcaa-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cfcaa-106">Convierte un tipo de **XLOPER**/ **XLOPER12** a otro o busca valores de celda en una hoja.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="cfcaa-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="cfcaa-107">Parameters</span></span>

 <span data-ttu-id="cfcaa-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="cfcaa-108">_pxSource_</span></span>
  
<span data-ttu-id="cfcaa-109">El **XLOPER XLOPER**/ de origen**XLOPER12** que debe convertirse.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="cfcaa-110">_pxDestType_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="cfcaa-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="cfcaa-111">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="cfcaa-111">(Optional).</span></span> <span data-ttu-id="cfcaa-112">Una máscara de bits de los tipos resultantes que desea aceptar.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="cfcaa-113">Debe usar el operador bit \*\*\*\* a bit or (|) para especificar varios tipos posibles.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="cfcaa-114">Si se omite este argumento, las referencias a celdas individuales se convierten en uno de los tipos de valor **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (si la celda a la que se hace referencia está vacía) y las referencias a bloques de celdas se convierten en **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-114">If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**.</span></span> <span data-ttu-id="cfcaa-115">Esto hace que **xlCoerce** sea la forma más cómoda de buscar valores de celda.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="cfcaa-116">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfcaa-116">Property value/Return value</span></span>

<span data-ttu-id="cfcaa-117">Devuelve el valor convertido (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**o **xltypeMulti**).</span><span class="sxs-lookup"><span data-stu-id="cfcaa-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cfcaa-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cfcaa-118">Remarks</span></span>

 <span data-ttu-id="cfcaa-119">**xlCoerce** no se puede convertir a o desde **xltypeBigData** o **xltypeFlow**.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-119">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**.</span></span> <span data-ttu-id="cfcaa-120">Pasar un tipo **xltypeMissing** o **xltypeNil** como _pxDestType_ equivale a omitir el argumento.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-120">Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument.</span></span> <span data-ttu-id="cfcaa-121">En algunos casos, se puede producir un error en la conversión.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-121">Conversion can fail in some cases.</span></span> <span data-ttu-id="cfcaa-122">Por ejemplo, algunas cadenas no se pueden convertir en números, mientras que otras pueden.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-122">For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="cfcaa-123">Si una matriz o una referencia de varias celdas se convierte en un tipo de valor único, el resultado es el valor de la celda superior izquierda o elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="cfcaa-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cfcaa-124">Example</span></span>

<span data-ttu-id="cfcaa-125">El siguiente código se puede encontrar en `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cfcaa-126">La función **xlcAlert** intenta convertir implícitamente su argumento en una cadena para que el paso de coerción que se muestra aquí se pudiera quitar de hecho, y **xInt** podría pasarse directamente a **xlcAlert**.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-126">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**.</span></span> <span data-ttu-id="cfcaa-127">Como **xlcAlert** es una macro de comando, este código sólo funciona correctamente cuando se llama desde una hoja de macros.</span><span class="sxs-lookup"><span data-stu-id="cfcaa-127">As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="cfcaa-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfcaa-128">See also</span></span>



[<span data-ttu-id="cfcaa-129">xlSet</span><span class="sxs-lookup"><span data-stu-id="cfcaa-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="cfcaa-130">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="cfcaa-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

