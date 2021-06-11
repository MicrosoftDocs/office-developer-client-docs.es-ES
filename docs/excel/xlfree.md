---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- función xlfree [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: de1c75ad65acacd44644e9bfb111b30abd0a578e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424717"
---
# <a name="xlfree"></a><span data-ttu-id="a49cd-104">xlFree</span><span class="sxs-lookup"><span data-stu-id="a49cd-104">xlFree</span></span>

 <span data-ttu-id="a49cd-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a49cd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a49cd-106">Se usa para liberar recursos de memoria asignados por Microsoft Excel al crear el valor devuelto **XLOPER** /  **XLOPER12** en una llamada a [Excel4,](excel4-excel12.md) [Excel4v,](excel4v-excel12v.md) [Excel12](excel4-excel12.md)o [Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="a49cd-106">Used to free memory resources allocated by Microsoft Excel when creating the return value **XLOPER**/ **XLOPER12** in a call to [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), or [Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="a49cd-107">La **función xlFree** libera la memoria auxiliar y restablece el puntero a **NULL,** pero no destruye otras partes de **XLOPER** /  **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="a49cd-107">The **xlFree** function frees the auxiliary memory and resets the pointer to **NULL** but does not destroy other parts of the **XLOPER**/ **XLOPER12**.</span></span>
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a><span data-ttu-id="a49cd-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="a49cd-108">Parameters</span></span>

 <span data-ttu-id="a49cd-109">_px_1, ..., px_n_</span><span class="sxs-lookup"><span data-stu-id="a49cd-109">_px_1, ..., px_n_</span></span>
  
<span data-ttu-id="a49cd-110">Uno o más **XLOPER** /  **XLOPER12** s que se liberarán.</span><span class="sxs-lookup"><span data-stu-id="a49cd-110">One or more **XLOPER**/ **XLOPER12** s to be freed.</span></span> <span data-ttu-id="a49cd-111">En Excel versiones anteriores a 2003, el número máximo de punteros que se pueden pasar es 30.</span><span class="sxs-lookup"><span data-stu-id="a49cd-111">In Excel versions up to 2003, the maximum number of pointers that can be passed is 30.</span></span> <span data-ttu-id="a49cd-112">A partir Excel 2007, se aumenta a 255.</span><span class="sxs-lookup"><span data-stu-id="a49cd-112">Starting in Excel 2007, this is increased to 255.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a49cd-113">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a49cd-113">Property value/Return value</span></span>

<span data-ttu-id="a49cd-114">Esta función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="a49cd-114">This function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a49cd-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a49cd-115">Remarks</span></span>

<span data-ttu-id="a49cd-116">Debe liberar cada **XLOPER** que obtenga como valor devuelto de **Excel4** o **Excel4v** y cada **XLOPER12** que obtenga como valor devuelto de **Excel12** o **Excel12v** si son uno de los siguientes tipos: **xltypeStr**, **xltypeMulti** o **xltypeRef**.</span><span class="sxs-lookup"><span data-stu-id="a49cd-116">You must free every **XLOPER** that you get as a return value from **Excel4** or **Excel4v** and every **XLOPER12** that you get as a return value from **Excel12** or **Excel12v** if they are one of the following types: **xltypeStr**, **xltypeMulti**, or **xltypeRef**.</span></span> <span data-ttu-id="a49cd-117">Siempre es seguro liberar otros tipos incluso si no usan memoria auxiliar, siempre y cuando los obtuvo de **Excel4** o **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="a49cd-117">It is always safe to free other types even if they do not use auxiliary memory, as long as you got them from **Excel4** or **Excel12**.</span></span>
  
<span data-ttu-id="a49cd-118">Cuando vuelva a Excel un puntero a un  /  **XLOPER XLOPER12** que aún contiene una memoria asignada Excel para liberarse, debe establecer **el xlbitXLFree** para asegurarse de que Excel libera la memoria.</span><span class="sxs-lookup"><span data-stu-id="a49cd-118">Where you are returning to Excel a pointer to an **XLOPER**/ **XLOPER12** that still contains Excel-allocated memory to be freed, you must set the **xlbitXLFree** to ensure Excel releases the memory.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a49cd-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a49cd-119">Example</span></span>

<span data-ttu-id="a49cd-120">En este ejemplo se llama **a GET. WORKSPACE(1) para** devolver la plataforma en la que Excel se está ejecutando actualmente como una cadena.</span><span class="sxs-lookup"><span data-stu-id="a49cd-120">This example calls **GET.WORKSPACE(1)** to return the platform on which Excel is currently running as a string.</span></span> <span data-ttu-id="a49cd-121">El código copia esta cadena devuelta en un búfer para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="a49cd-121">The code copies this returned string into a buffer for later use.</span></span> <span data-ttu-id="a49cd-122">El código coloca el búfer de nuevo en **XLOPER12** para su uso posterior con la Excel función.</span><span class="sxs-lookup"><span data-stu-id="a49cd-122">The code places the buffer back into the **XLOPER12** for later use with the Excel function.</span></span> <span data-ttu-id="a49cd-123">Por último, el código muestra la cadena en un cuadro de alerta.</span><span class="sxs-lookup"><span data-stu-id="a49cd-123">Finally, the code displays the string in an alert box.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="a49cd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a49cd-124">See also</span></span>

- [<span data-ttu-id="a49cd-125">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="a49cd-125">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

