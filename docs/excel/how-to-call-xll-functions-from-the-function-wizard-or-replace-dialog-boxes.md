---
title: Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo reemplazar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funciones XLL [Excel 2007], llamar desde el cuadro de diálogo reemplazar, cuadro de diálogo reemplazar [Excel 2007], llamar a funciones XLL, Asistente para funciones [Excel 2007], llamar a funciones XLL, funciones XLL [Excel 2007], llamar desde el Asistente para funciones
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11189beed13e2ceb99ef04b7a2f966cb4171915c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304021"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a>Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo reemplazar

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel suele llamar a funciones XLL durante el recálculo normal del libro, o parte de él si el cálculo está bajo el control de una macro. Recuerde que la función puede que no resida en una fórmula de celda, pero que puede formar parte de una definición de rango con nombre o una expresión de formato condicional.
  
Hay dos situaciones en las que se puede llamar a una función desde un cuadro de diálogo de Excel. Uno es el cuadro de diálogo **pegar argumentos de función** , en el que los usuarios pueden crear una llamada de función en un argumento cada vez. La otra es cuando las fórmulas se modifican y se reescriben mediante Excel en el cuadro de diálogo **reemplazar** . En el cuadro de diálogo **pegar argumentos de función** , es posible que no desee que la función se ejecute con normalidad. Esto puede deberse a que tarda mucho tiempo en ejecutarse y no desea reducir el uso del cuadro de diálogo. 
  
Tanto el cuadro de diálogo **pegar función** como el cuadro de diálogo **reemplazar** tienen el nombre de la clase de Windows **bosa_sdm_XL**n, donde n es un número. Windows proporciona una función de la API, **getClassName**, que obtiene este nombre de un identificador de Windows, un tipo de variable HWND. También proporciona otra función, **EnumWindows**, que llama a una función de devolución de llamada suministrada (dentro de la dll) una vez por cada ventana de nivel superior que esté abierta en ese momento.
  
La función de devolución de llamada debe realizar solo los pasos siguientes:
  
1. Compruebe si el elemento primario de esta ventana es la instancia actual de Excel (en caso de que haya varias instancias en ejecución).
    
2. Obtiene el nombre de clase del identificador que se ha pasado en Windows.
    
3. Compruebe si el nombre de clase tiene el formato **bosa_sdm_XL**n.
    
4. Si necesita distinguir entre los dos cuadros de diálogo, compruebe si el título del cuadro de diálogo contiene algún texto identificativo. El título de la ventana se obtiene mediante la **GetWindowText**de llamada API de Windows.
    
El siguiente código C++ muestra una clase y una devolución de llamada que se pasa a Windows que realiza estos pasos. Esto es invocado por las funciones que llaman específicamente a test para cualquiera de los cuadros de diálogo en cuestión. 
  
> [!NOTE]
> Los títulos de ventana de futuras versiones de Excel podrían cambiar e invalidar este código. Tenga en cuenta también que la configuración de **window_title_text** en **null** tiene el efecto de omitir el título de la ventana en la búsqueda de devolución de llamada. 
  
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

El cuadro de diálogo **pegar función** no tiene título, por lo que la siguiente función pasa la cadena del título de búsqueda "", es decir, una cadena vacía, a la devolución de llamada para indicar que la condición de coincidencia es que la ventana no debe tener un título. 
  
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

## <a name="see-also"></a>Vea también



[Obtener acceso a código XLL en Excel](accessing-xll-code-in-excel.md)
  
[Llamar a Excel desde el archivo DLL o XLL](calling-into-excel-from-the-dll-or-xll.md)
  
[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)

