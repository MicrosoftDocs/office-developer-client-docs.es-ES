---
title: Llamar a funciones XLL desde el Asistente para funciones o reemplazar cuadros de diálogo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Funciones xll [excel 2007], llamadas desde el cuadro de diálogo reemplazar,Cuadro de diálogo Reemplazar [Excel 2007], llamar a funciones XLL,Asistente para funciones [Excel 2007], llamar a funciones XLL,funciones XLL [Excel 2007], llamar desde el Asistente para funciones
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11189beed13e2ceb99ef04b7a2f966cb4171915c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410752"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a><span data-ttu-id="07140-104">Llamar a funciones XLL desde el Asistente para funciones o reemplazar cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="07140-104">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>

 <span data-ttu-id="07140-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="07140-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="07140-106">Microsoft Excel llamadas a funciones XLL durante el recálculo normal del libro, o una parte de él si el cálculo está bajo el control de una macro.</span><span class="sxs-lookup"><span data-stu-id="07140-106">Microsoft Excel usually calls XLL functions during the normal recalculation of the workbook, or a part of it if the calculation is under the control of a macro.</span></span> <span data-ttu-id="07140-107">Recuerde que es posible que la función no resida en una fórmula de celda, pero puede formar parte de una definición de intervalo con nombre o de una expresión de formato condicional.</span><span class="sxs-lookup"><span data-stu-id="07140-107">Remember that the function might not reside in a cell formula but might be part of a named range definition, or a conditional formatting expression.</span></span>
  
<span data-ttu-id="07140-108">Hay dos circunstancias en las que se puede llamar a una función desde un Excel de diálogo.</span><span class="sxs-lookup"><span data-stu-id="07140-108">There are two circumstances where a function can be called from an Excel dialog box.</span></span> <span data-ttu-id="07140-109">Uno es el **cuadro de diálogo Pegar argumentos** de función, donde los usuarios pueden construir una llamada a función de un argumento a la vez.</span><span class="sxs-lookup"><span data-stu-id="07140-109">One is the **Paste Function Arguments** dialog box, where users are able to construct a function call one argument at a time.</span></span> <span data-ttu-id="07140-110">La otra es cuando las fórmulas se modifican y se vuelve a introducir Excel en el **cuadro de** diálogo Reemplazar.</span><span class="sxs-lookup"><span data-stu-id="07140-110">The other is when formulas are being modified and reentered by Excel in the **Replace** dialog box.</span></span> <span data-ttu-id="07140-111">Para el **cuadro de diálogo Pegar argumentos** de función, es posible que no desee que la función se ejecute normalmente.</span><span class="sxs-lookup"><span data-stu-id="07140-111">For the **Paste Function Arguments** dialog box, you might not want your function to execute normally.</span></span> <span data-ttu-id="07140-112">Esto puede deberse a que tarda mucho tiempo en ejecutarse y no desea ralentizar el uso del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="07140-112">This may be because it takes a long time to execute and you do not want to slow down the use of the dialog box.</span></span> 
  
<span data-ttu-id="07140-113">Tanto el **cuadro de**  diálogo Pegar función como el cuadro de diálogo Reemplazar tienen el Windows de clase bosa_sdm_XL **n,** donde n es un número.</span><span class="sxs-lookup"><span data-stu-id="07140-113">Both the **Paste Function** dialog box and the **Replace** dialog box have the Windows class name **bosa_sdm_XL** n, where n is a number.</span></span> <span data-ttu-id="07140-114">Windows proporciona una función api, **GetClassName**, que obtiene este nombre de un identificador Windows, un tipo de variable HWND.</span><span class="sxs-lookup"><span data-stu-id="07140-114">Windows provides an API function, **GetClassName**, that obtains this name from a Windows handle, an HWND variable type.</span></span> <span data-ttu-id="07140-115">También proporciona otra función, **EnumWindows**, que llama a una función de devolución de llamada suministrada (dentro de la DLL) una vez por cada ventana de nivel superior que esté abierta actualmente.</span><span class="sxs-lookup"><span data-stu-id="07140-115">It also provides another function, **EnumWindows**, that calls a supplied callback function (within your DLL) once for every top-level window that is currently open.</span></span>
  
<span data-ttu-id="07140-116">La función de devolución de llamada solo debe realizar los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="07140-116">The callback function needs to perform only the following steps:</span></span>
  
1. <span data-ttu-id="07140-117">Compruebe si el elemento principal de esta ventana es la instancia actual de Excel (en caso de que haya varias instancias en ejecución).</span><span class="sxs-lookup"><span data-stu-id="07140-117">Check if the parent of this window is the current instance of Excel (in case there are multiple instances running).</span></span>
    
2. <span data-ttu-id="07140-118">Obtener el nombre de clase del identificador pasado por Windows.</span><span class="sxs-lookup"><span data-stu-id="07140-118">Get the class name from the handle passed in by Windows.</span></span>
    
3. <span data-ttu-id="07140-119">Compruebe si el nombre de clase es del formulario **bosa_sdm_XL** n.</span><span class="sxs-lookup"><span data-stu-id="07140-119">Check if the class name is of the form **bosa_sdm_XL** n.</span></span>
    
4. <span data-ttu-id="07140-120">Si necesita distinguir entre los dos cuadros de diálogo, compruebe si el título del cuadro de diálogo contiene texto identificativos.</span><span class="sxs-lookup"><span data-stu-id="07140-120">If you need to distinguish between the two dialog boxes, check if the dialog box title contains some identifying text.</span></span> <span data-ttu-id="07140-121">El título de la ventana se obtiene mediante la llamada Windows API **GetWindowText**.</span><span class="sxs-lookup"><span data-stu-id="07140-121">The window title is obtained using the Windows API call **GetWindowText**.</span></span>
    
<span data-ttu-id="07140-122">El siguiente código de C++ muestra una clase y una devolución de llamada que se deben pasar a Windows que realiza estos pasos.</span><span class="sxs-lookup"><span data-stu-id="07140-122">The following C++ code shows a class and callback to be passed to Windows that performs these steps.</span></span> <span data-ttu-id="07140-123">A esto llaman las funciones que llaman a la prueba específicamente para cualquiera de los cuadros de diálogo correspondientes.</span><span class="sxs-lookup"><span data-stu-id="07140-123">This is called by the functions that call test specifically for either of the dialog boxes concerned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="07140-124">Los títulos de ventana de Excel versiones futuras pueden cambiar e invalidar este código.</span><span class="sxs-lookup"><span data-stu-id="07140-124">Window titles of future Excel versions might change and invalidate this code.</span></span> <span data-ttu-id="07140-125">Tenga en cuenta también **que window_title_text** en **NULL** tiene el efecto de ignorar el título de la ventana en la búsqueda de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="07140-125">Note also that setting **window_title_text** to **NULL** has the effect of ignoring window title in the callback search.</span></span> 
  
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

<span data-ttu-id="07140-126">El  cuadro de diálogo Función pegar no tiene un título, por lo que la siguiente función pasa una cadena de título de búsqueda de "", es decir, una cadena vacía, a la devolución de llamada para indicar que la condición de coincidencia es que la ventana no debe tener un título.</span><span class="sxs-lookup"><span data-stu-id="07140-126">The **Paste Function** dialog box does not have a title, so the following function passes a search title string of "", that is, an empty string, to the callback to indicate that the match condition is that the window should not have a title.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="07140-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="07140-127">See also</span></span>



[<span data-ttu-id="07140-128">Obtener acceso a código XLL en Excel</span><span class="sxs-lookup"><span data-stu-id="07140-128">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
[<span data-ttu-id="07140-129">Llamar a Excel desde el archivo DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="07140-129">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
[<span data-ttu-id="07140-130">Desarrollar archivos XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="07140-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

