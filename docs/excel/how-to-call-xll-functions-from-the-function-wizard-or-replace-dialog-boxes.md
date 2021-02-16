---
title: Llamar a funciones XLL desde el Asistente para funciones o cuadros de diálogo Reemplazar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Funciones xll [excel 2007], llamada desde cuadro de diálogo de reemplazo,cuadro de diálogo Reemplazar [Excel 2007], llamada a funciones XLL,Asistente para funciones [Excel 2007], llamada a funciones XLL,Funciones XLL [Excel 2007], llamada desde el Asistente para funciones
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
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a>Llamar a funciones XLL desde el Asistente para funciones o cuadros de diálogo Reemplazar

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel normalmente llama a funciones XLL durante la actualización normal del libro, o una parte de él si el cálculo está bajo el control de una macro. Recuerde que es posible que la función no resida en una fórmula de celda, pero puede formar parte de una definición de rango con nombre o de una expresión de formato condicional.
  
Existen dos circunstancias en las que se puede llamar a una función desde un cuadro de diálogo de Excel. Uno es el **cuadro de diálogo Pegar argumentos** de función, donde los usuarios pueden construir una llamada de función un argumento a la vez. La otra es cuando Excel modifica y vuelve a escribir las fórmulas en el **cuadro de** diálogo Reemplazar. Para el **cuadro de diálogo Pegar argumentos** de función, es posible que no desee que la función se ejecute normalmente. Esto puede deberse a que se tarda mucho tiempo en ejecutarse y no se desea ralentizar el uso del cuadro de diálogo. 
  
Tanto el **cuadro de**  diálogo Pegar función como el cuadro de diálogo Reemplazar tienen el nombre de clase de Windows **bosa_sdm_XL** n, donde n es un número. Windows proporciona una función de API, **GetClassName**, que obtiene este nombre de un identificador de Windows, un tipo de variable HWND. También proporciona otra función, **EnumWindows,** que llama a una función de devolución de llamada proporcionada (dentro de la DLL) una vez por cada ventana de nivel superior que está abierta actualmente.
  
La función de devolución de llamada solo necesita realizar los siguientes pasos:
  
1. Compruebe si el elemento principal de esta ventana es la instancia actual de Excel (en caso de que haya varias instancias en ejecución).
    
2. Obtén el nombre de clase del identificador pasado por Windows.
    
3. Compruebe si el nombre de clase tiene el formato **bosa_sdm_XL** n.
    
4. Si necesita distinguir entre los dos cuadros de diálogo, compruebe si el título del cuadro de diálogo contiene texto identificativos. El título de la ventana se obtiene mediante la llamada de la API de Windows **GetWindowText**.
    
El siguiente código C++ muestra una clase y una devolución de llamada que se pasan a Windows que realiza estos pasos. Lo llaman las funciones que llaman a la prueba específicamente para cualquiera de los cuadros de diálogo correspondientes. 
  
> [!NOTE]
> Los títulos de ventana de futuras versiones de Excel pueden cambiar e invalidar este código. Tenga en cuenta también **que window_title_text** **en NULL** tiene el efecto de omitir el título de la ventana en la búsqueda de devolución de llamada. 
  
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

El  cuadro de diálogo Pegar función no tiene un título, por lo que la siguiente función pasa una cadena de título de búsqueda de "", es decir, una cadena vacía, a la devolución de llamada para indicar que la condición de coincidencia es que la ventana no debe tener un título. 
  
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

## <a name="see-also"></a>Consulte también



[Obtener acceso a código XLL en Excel](accessing-xll-code-in-excel.md)
  
[Llamar a Excel desde el archivo DLL o XLL](calling-into-excel-from-the-dll-or-xll.md)
  
[Desarrollar archivos XLL de Excel](developing-excel-xlls.md)

