---
title: Obtener acceso a la instancia de Excel y los controladores de la ventana principal
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- obtener acceso a de controladores, controladores [Excel 2007], obtener acceso a las instancias de Excel, obtener acceso a los identificadores de ventana [Excel 2007], obtener acceso a excel
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 035cd2a8423e3ab14f4b2ca4b73fbc39641e54d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815651"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Obtener acceso a la instancia de Excel y los controladores de la ventana principal

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
A veces para programar en el entorno de Windows, debe conocer el identificador de la instancia de Microsoft Excel o la ventana principal de administrar. Por ejemplo, estos controladores son útiles cuando se están creando y mostrar cuadros de diálogo de Windows personalizados.
  
Hay dos funciones de la API de C sólo XLL que proporcionan acceso a estos controladores: la función [xlGetInst](xlgetinst.md) y la [xlGetHwnd](xlgethwnd.md) funcionan respectivamente. En Win32, todos los identificadores son números enteros de 32 bits. Sin embargo, cuando se diseñó el **XLOPER** , Windows era un sistema de 16 bits. Por lo tanto, la estructura que sólo se permite para controladores de 16 bits. En Win32, cuando se llama con **Excel4** o **Excel4v**, la función **xlGetInst** y la función **xlGetHwnd** devuelven sólo la parte baja del identificador de 32 bits completa. 
  
En Excel 2007 y versiones posteriores, cuando se llaman a estas funciones con [Excel12](excel4-excel12.md) o [Excel12v](excel4v-excel12v.md), **XLOPER12** devuelto contiene un controlador de 32 bits. 
  
Obtener el identificador de instancia completa es simple en cualquier versión de Excel, tal como se pasa a la devolución de llamada de Windows **DllMain**, que se llama cuando se carga el archivo DLL. Si registrar este identificador de instancia en una variable global, nunca debe llamar a la función **xlGetInst** . 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Obtener el identificador principal de Excel en Excel 2003 y versiones anteriores

Para obtener el identificador principal de Excel en Excel 2003 y versiones anteriores de 32 bits, primero debe llamar a la función **xlGetHwnd** para obtener la palabra baja del identificador real. A continuación, debe recorrer en iteración la lista de ventanas de nivel superior para buscar una coincidencia con la palabra baja devuelta. El siguiente código muestra la técnica. 
  
```cs
typedef struct _EnumStruct
{
  HWND hwnd;  // Return value for Excel main hWnd.
  unsigned short wLoword; //Contains LowWord of the Excel main hWnd
} EnumStruct;
#define CLASS_NAME_BUFFER  50
BOOL CALLBACK EnumProc(HWND hwnd, EnumStruct * pEnum)
{
  // First check the class of the window. Must be "XLMAIN".
  char rgsz[CLASS_NAME_BUFFER];
  GetClassName(hwnd, rgsz, CLASS_NAME_BUFFER);
  if (!lstrcmpi(rgsz, "XLMAIN"))
  {
    // If that hits, check the loword of the window handle.
    if (LOWORD((DWORD) hwnd) == pEnum->wLoword)
    {
      // We have a match, return Excel main hWnd.
      pEnum->hwnd = hwnd;
      return FALSE;
    }
  }
  // No match - continue the enumeration.
  return TRUE;
}
BOOL GetHwnd(HWND * pHwnd)
{
  XLOPER x;
  //
  // xlGetHwnd only returns the LoWord of Excel hWnd
  // so all the windows have to be enumerated to see
  // which match the LoWord retuned by xlGetHwnd.
  //
  if (Excel4(xlGetHwnd, &x, 0) == xlretSuccess)
  {
    EnumStruct enm;
    enm.hwnd = NULL;
    enm.wLoword = x.val.w;
    EnumWindows((WNDENUMPROC) EnumProc, (LPARAM) &enm);
    if (enm.hwnd != NULL)
    {
      *pHwnd = enm.hwnd;
      return TRUE;
    }
  }
  return FALSE;
}
```

## <a name="see-also"></a>Vea también



[Mostrar cuadros de diálogo de un DLL o XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)

