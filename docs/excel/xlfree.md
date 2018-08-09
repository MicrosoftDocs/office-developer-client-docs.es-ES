---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- función xlFree [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2dd61ee5cd0e2e671cc47425689287b8a437732f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815738"
---
# <a name="xlfree"></a><span data-ttu-id="7dbf8-104">xlFree</span><span class="sxs-lookup"><span data-stu-id="7dbf8-104">xlFree</span></span>

 <span data-ttu-id="7dbf8-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7dbf8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7dbf8-106">Usado para liberar memoria recursos asignados por Microsoft Excel al crear la devolución de valor **XLOPER**/ **XLOPER12** en una llamada a [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)o [Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="7dbf8-106">Used to free memory resources allocated by Microsoft Excel when creating the return value **XLOPER**/ **XLOPER12** in a call to [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), or [Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="7dbf8-107">La función **xlFree** libera la memoria auxiliar y restablece el puntero en **NULL** , pero no destruye otras partes de la **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="7dbf8-107">The **xlFree** function frees the auxiliary memory and resets the pointer to **NULL** but does not destroy other parts of the **XLOPER**/ **XLOPER12**.</span></span>
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a><span data-ttu-id="7dbf8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7dbf8-108">Parameters</span></span>

 <span data-ttu-id="7dbf8-109">_px_1,..., px_n_</span><span class="sxs-lookup"><span data-stu-id="7dbf8-109">_px_1, ..., px_n_</span></span>
  
<span data-ttu-id="7dbf8-110">Uno o más **XLOPER**/ s**XLOPER12**liberarse.</span><span class="sxs-lookup"><span data-stu-id="7dbf8-110">One or more **XLOPER**/ **XLOPER12**s to be freed.</span></span> <span data-ttu-id="7dbf8-111">En las versiones de Excel hasta 2003, el número máximo de punteros que se pueden pasar es 30.</span><span class="sxs-lookup"><span data-stu-id="7dbf8-111">In Excel versions up to 2003, the maximum number of pointers that can be passed is 30.</span></span> <span data-ttu-id="7dbf8-112">Iniciar en Excel 2007, se aumenta a 255.</span><span class="sxs-lookup"><span data-stu-id="7dbf8-112">Starting in Excel 2007, this is increased to 255.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="7dbf8-113">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7dbf8-113">Property value/Return value</span></span>

<span data-ttu-id="7dbf8-114">Esta función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="7dbf8-114">This function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7dbf8-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7dbf8-115">Remarks</span></span>

<span data-ttu-id="7dbf8-116">Debe liberar cada **XLOPER** que se obtiene como un valor devuelto de **Excel4** o **Excel4v** y cada **XLOPER12** que se obtiene como valor devuelto desde **Excel12** o **Excel12v** si son uno de los siguientes tipos: xltypeStr ** **, **xltypeMulti**o **xltypeRef**.</span><span class="sxs-lookup"><span data-stu-id="7dbf8-116">You must free every **XLOPER** that you get as a return value from **Excel4** or **Excel4v** and every **XLOPER12** that you get as a return value from **Excel12** or **Excel12v** if they are one of the following types: **xltypeStr**, **xltypeMulti**, or **xltypeRef**.</span></span> <span data-ttu-id="7dbf8-117">Siempre es seguro libre a otros tipos incluso si no usan memoria auxiliar, siempre que obtuvo de **Excel4** o **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="7dbf8-117">It is always safe to free other types even if they do not use auxiliary memory, as long as you got them from **Excel4** or **Excel12**.</span></span>
  
<span data-ttu-id="7dbf8-118">Donde se va a devolver a Excel un puntero a un **XLOPER**/ **XLOPER12** que aún contiene memoria asignada de Excel que se va a liberar, debe establecer el **xlbitXLFree** para garantizar la memoria de versiones de Excel.</span><span class="sxs-lookup"><span data-stu-id="7dbf8-118">Where you are returning to Excel a pointer to an **XLOPER**/ **XLOPER12** that still contains Excel-allocated memory to be freed, you must set the **xlbitXLFree** to ensure Excel releases the memory.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7dbf8-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7dbf8-119">Example</span></span>

<span data-ttu-id="7dbf8-120">En este ejemplo se llama **obtener. WORKSPACE(1)** para devolver la plataforma en que Excel se está ejecutando como una cadena.</span><span class="sxs-lookup"><span data-stu-id="7dbf8-120">This example calls **GET.WORKSPACE(1)** to return the platform on which Excel is currently running as a string.</span></span> <span data-ttu-id="7dbf8-121">El código copia este valor devuelto de cadena en un búfer para usarlo más adelante.</span><span class="sxs-lookup"><span data-stu-id="7dbf8-121">The code copies this returned string into a buffer for later use.</span></span> <span data-ttu-id="7dbf8-122">El código coloca el búfer de copia en el **XLOPER12** para usarlo más adelante con la función de Excel.</span><span class="sxs-lookup"><span data-stu-id="7dbf8-122">The code places the buffer back into the **XLOPER12** for later use with the Excel function.</span></span> <span data-ttu-id="7dbf8-123">Por último, el código muestra la cadena en un cuadro de alerta.</span><span class="sxs-lookup"><span data-stu-id="7dbf8-123">Finally, the code displays the string in an alert box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="7dbf8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7dbf8-124">See also</span></span>

- [<span data-ttu-id="7dbf8-125">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="7dbf8-125">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

