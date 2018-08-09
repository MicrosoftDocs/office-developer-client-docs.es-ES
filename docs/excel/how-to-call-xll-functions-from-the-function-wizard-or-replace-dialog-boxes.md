---
title: Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo Reemplazar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funciones XLL [excel 2007], llamar desde el cuadro de diálogo Reemplazar, cuadro de diálogo Reemplazar cuadro [Excel 2007], llamada a funciones XLL, Asistente para funciones [Excel 2007], llamar a funciones XLL, funciones XLL [Excel 2007], llamar desde el Asistente para funciones
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7ebb33a5b98cebedfca7fb5923e62486bfd85696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815648"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a><span data-ttu-id="f2a3f-104">Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo Reemplazar</span><span class="sxs-lookup"><span data-stu-id="f2a3f-104">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>

 <span data-ttu-id="f2a3f-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f2a3f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f2a3f-106">Microsoft Excel llama normalmente funciones XLL durante la actualización normal del libro o una parte del mismo si el cálculo es bajo el control de una macro.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-106">Microsoft Excel usually calls XLL functions during the normal recalculation of the workbook, or a part of it if the calculation is under the control of a macro.</span></span> <span data-ttu-id="f2a3f-107">Recuerde que la función no puede residir en una fórmula de celda, pero es posible que forme parte de una definición de rango con nombre, o una expresión de formato condicional.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-107">Remember that the function might not reside in a cell formula but might be part of a named range definition, or a conditional formatting expression.</span></span>
  
<span data-ttu-id="f2a3f-108">Hay dos casos donde se puede llamar una función desde un cuadro de diálogo de Excel.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-108">There are two circumstances where a function can be called from an Excel dialog box.</span></span> <span data-ttu-id="f2a3f-109">Uno es el cuadro de diálogo **Argumentos de la función Pegar** , donde los usuarios tienen construir un una argumento llamada de función a la vez.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-109">One is the **Paste Function Arguments** dialog box, where users are able to construct a function call one argument at a time.</span></span> <span data-ttu-id="f2a3f-110">La otra es cuando las fórmulas se va a modificar y volver a introducir por Excel en el cuadro de diálogo **Reemplazar** .</span><span class="sxs-lookup"><span data-stu-id="f2a3f-110">The other is when formulas are being modified and reentered by Excel in the **Replace** dialog box.</span></span> <span data-ttu-id="f2a3f-111">Para el cuadro de diálogo **Argumentos de la función Pegar** , es posible que no desea que su función para ejecutarse con normalidad.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-111">For the **Paste Function Arguments** dialog box, you might not want your function to execute normally.</span></span> <span data-ttu-id="f2a3f-112">Esto puede deberse a que tarda mucho tiempo en ejecutarse y no desea que se ralentice el uso del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-112">This may be because it takes a long time to execute and you do not want to slow down the use of the dialog box.</span></span> 
  
<span data-ttu-id="f2a3f-113">El cuadro de diálogo **Pegar función** y el cuadro de diálogo **Reemplazar** tienen el nombre de clase Windows **bosa_sdm_XL**n, donde n es un número.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-113">Both the **Paste Function** dialog box and the **Replace** dialog box have the Windows class name **bosa_sdm_XL**n, where n is a number.</span></span> <span data-ttu-id="f2a3f-114">Windows proporciona una función de la API, **GetClassName**, que obtiene este nombre de un identificador de Windows, un tipo de variable de HWND.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-114">Windows provides an API function, **GetClassName**, that obtains this name from a Windows handle, an HWND variable type.</span></span> <span data-ttu-id="f2a3f-115">También proporciona otra función, **EnumWindows**, que llama a una función de devolución de llamada suministrado (dentro de la DLL) una vez para cada ventana de nivel superior que está actualmente abierto.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-115">It also provides another function, **EnumWindows**, that calls a supplied callback function (within your DLL) once for every top-level window that is currently open.</span></span>
  
<span data-ttu-id="f2a3f-116">Las necesidades de la función de devolución de llamada para llevar a cabo sólo los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="f2a3f-116">The callback function needs to perform only the following steps:</span></span>
  
1. <span data-ttu-id="f2a3f-117">Compruebe si el elemento primario de esta ventana es la instancia actual de Excel (en caso de que no hay varias instancias en ejecución).</span><span class="sxs-lookup"><span data-stu-id="f2a3f-117">Check if the parent of this window is the current instance of Excel (in case there are multiple instances running).</span></span>
    
2. <span data-ttu-id="f2a3f-118">Obtener el nombre de clase desde el controlador que se pasó por parte de Windows.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-118">Get the class name from the handle passed in by Windows.</span></span>
    
3. <span data-ttu-id="f2a3f-119">Compruebe si es el nombre de clase de formulario **bosa_sdm_XL**n.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-119">Check if the class name is of the form **bosa_sdm_XL**n.</span></span>
    
4. <span data-ttu-id="f2a3f-120">Si necesita distinguir entre los dos cuadros de diálogo, compruebe si el título del cuadro de diálogo contiene algún texto de identificación.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-120">If you need to distinguish between the two dialog boxes, check if the dialog box title contains some identifying text.</span></span> <span data-ttu-id="f2a3f-121">El título de la ventana se obtiene mediante la llamada de API de Windows **GetWindowText**.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-121">The window title is obtained using the Windows API call **GetWindowText**.</span></span>
    
<span data-ttu-id="f2a3f-122">El código de C++ siguiente muestra una clase y una devolución de llamada que se pasan a Windows que lleva a cabo estos pasos.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-122">The following C++ code shows a class and callback to be passed to Windows that performs these steps.</span></span> <span data-ttu-id="f2a3f-123">Esto se denomina por las funciones de llamada de prueba específicamente para cualquiera de los cuadros de diálogo que se trate.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-123">This is called by the functions that call test specifically for either of the dialog boxes concerned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f2a3f-124">Es posible que cambie los títulos de ventana de futuras versiones de Excel y se invalidar este código.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-124">Window titles of future Excel versions might change and invalidate this code.</span></span> <span data-ttu-id="f2a3f-125">Tenga en cuenta también que si el valor de **window_title_text** es **NULL** tiene el efecto de omitir el título de la ventana en la búsqueda de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-125">Note also that setting **window_title_text** to **NULL** has the effect of ignoring window title in the callback search.</span></span> 
  
```cs
#define CLASS_NAME_BUFFSIZE  50
#define WINDOW_TEXT_BUFFSIZE  50
// Data structure used as input to xldlg_enum_proc(), called by
// called_from_paste_fn_dlg(), called_from_replace_dlg(), and
// called_from_Excel_dlg(). These functions tell the caller whether
// the current worksheet function was called from one or either of
// these dialog boxes.
typedef struct
{
  bool is_dlg;
  short low_hwnd;
  char *window_title_text; // set to NULL if don't care
}
  xldlg_enum_struct;
// The callback function called by Windows for every top-level window.
BOOL CALLBACK xldlg_enum_proc(HWND hwnd, xldlg_enum_struct *p_enum)
{
// Check if the parent window is Excel.
// Note: Because of the change from MDI (Excel 2010)
// to SDI (Excel 2013), comment out this step in Excel 2013.
  if(LOWORD((DWORD)GetParent(hwnd)) != p_enum->low_hwnd)
    return TRUE; // keep iterating
  char class_name[CLASS_NAME_BUFFSIZE + 1];
//  Ensure that class_name is always null terminated for safety.
  class_name[CLASS_NAME_BUFFSIZE] = 0;
  GetClassName(hwnd, class_name, CLASS_NAME_BUFFSIZE);
//  Do a case-insensitve comparison for the Excel dialog window
//  class name with the Excel version number truncated.
  size_t len; // The length of the window's title text
  if(_strnicmp(class_name, "bosa_sdm_xl", 11) == 0)
  {
// Check if a searching for a specific title string
    if(p_enum->window_title_text) 
    {
// Get the window's title and see if it matches the given text.
      char buffer[WINDOW_TEXT_BUFFSIZE + 1];
      buffer[WINDOW_TEXT_BUFFSIZE] = 0;
      len = GetWindowText(hwnd, buffer, WINDOW_TEXT_BUFFSIZE);
      if(len == 0) // No title
      {
        if(p_enum->window_title_text[0] != 0)
          return TRUE; // No match, so keep iterating
      }
// Window has a title so do a case-insensitive comparison of the
// title and the search text, if provided.
      else if(p_enum->window_title_text[0] != 0
      && _stricmp(buffer, p_enum->window_title_text) != 0)
        return TRUE; // Keep iterating
    }
    p_enum->is_dlg = true;
    return FALSE; // Tells Windows to stop iterating.
  }
  return TRUE; // Tells Windows to continue iterating.
}
```

<span data-ttu-id="f2a3f-126">El cuadro de diálogo **Pegar función** no tiene un título, por lo que la siguiente función pasa una cadena de título de la búsqueda de "", es decir, una cadena vacía, a la devolución de llamada para indicar que la condición de coincidencia es que la ventana no debe tener un título.</span><span class="sxs-lookup"><span data-stu-id="f2a3f-126">The **Paste Function** dialog box does not have a title, so the following function passes a search title string of "", that is, an empty string, to the callback to indicate that the match condition is that the window should not have a title.</span></span> 
  
```cs
bool called_from_paste_fn_dlg(void)
{
    XLOPER xHwnd;
// Calls Excel4, which only returns the low part of the Excel
// main window handle. This is OK for the search however.
    if(Excel4(xlGetHwnd, &xHwnd, 0))
        return false; // Couldn't get it, so assume not
// Search for bosa_sdm_xl* dialog box with no title string.
    xldlg_enum_struct es = {FALSE, xHwnd.val.w, ""};
    EnumWindows((WNDENUMPROC)xldlg_enum_proc, (LPARAM)&es);
    return es.is_dlg;
}
```

## <a name="see-also"></a><span data-ttu-id="f2a3f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2a3f-127">See also</span></span>



[<span data-ttu-id="f2a3f-128">Obtener acceso a código XLL en Excel</span><span class="sxs-lookup"><span data-stu-id="f2a3f-128">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
[<span data-ttu-id="f2a3f-129">Llamar a Excel desde el archivo DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="f2a3f-129">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
[<span data-ttu-id="f2a3f-130">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="f2a3f-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

