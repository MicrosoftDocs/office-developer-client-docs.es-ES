---
title: Controladores de instancia de Excel y ventana principal
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- obtener acceso a identificadores de Excel, controles [Excel 2007], acceso, instancias de Excel, obtener acceso, identificadores de ventana [Excel 2007], obtener acceso
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4b71ccd428e60c9ba2e59fea0e56eb2fc61390db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310762"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Controladores de instancia de Excel y ventana principal

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para programar en el entorno de Windows, a veces es necesario conocer el identificador de instancia o de ventana principal de Microsoft Excel. Por ejemplo, estos controladores resultan útiles cuando se crean y muestran cuadros de diálogo personalizados de Windows.
  
Hay dos funciones API de C de solo XLL que proporcionan acceso a estos identificadores: la función [xlGetInst](xlgetinst.md) y la función [xlGetHwnd](xlgethwnd.md) respectivamente. En Win32, todos los identificadores son enteros de 32 bits. Sin embargo, cuando se diseñó **XLOPER** , Windows era un sistema de 16 bits. Por lo tanto, la estructura solo se permite para los identificadores de 16 bits. En Win32, cuando se llama con **Excel4** o **Excel4v**, la función **xlGetInst** y la función **xlGetHwnd** solo devuelven la parte baja del identificador completo de 32 bits. 
  
En Excel 2007 y versiones posteriores, cuando se llama a estas funciones con [Excel12](excel4-excel12.md) o [Excel12v](excel4v-excel12v.md), el **XLOPER12** devuelto contiene el identificador de 32 bits completo. 
  
La obtención del controlador de instancia completo es sencilla en cualquier versión de Excel, ya que se pasa a la **DllMain**de devolución de llamada de Windows, a la que se llama cuando se carga el archivo dll. Si graba este controlador de instancia en una variable global, nunca tendrá que llamar a la función **xlGetInst** . 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Obtener el controlador principal de Excel en Excel 2003 y versiones anteriores

Para obtener el controlador principal de Excel en Excel 2003 y versiones anteriores de 32 bits, debe llamar primero a la función **xlGetHwnd** para obtener la palabra inferior del controlador real. A continuación, debe iterar la lista de ventanas de nivel superior para buscar una coincidencia con la palabra baja devuelta. El siguiente código ilustra la técnica. 
  
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
  // which match the LoWord returned by xlGetHwnd.
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



[Mostrar cuadros de diálogo desde una DLL o XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)

