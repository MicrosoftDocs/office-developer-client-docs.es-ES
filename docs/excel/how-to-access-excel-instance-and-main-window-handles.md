---
title: Identificadores Excel instancia y ventana principal de Access
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- acceso a controladores de excel, controladores [Excel 2007], acceso Excel instancias, acceso, identificadores de ventana [Excel 2007], acceso a
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
# <a name="access-excel-instance-and-main-window-handles"></a>Identificadores Excel instancia y ventana principal de Access

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para programar en el entorno Windows, a veces debe conocer el identificador Microsoft Excel instancia o el identificador de ventana principal. Por ejemplo, estos controladores son útiles al crear y mostrar cuadros de diálogo de Windows personalizados.
  
Hay dos funciones de API de C solo XLL que proporcionan acceso a estos controladores: la función [xlGetInst](xlgetinst.md) y la función [xlGetHwnd](xlgethwnd.md) respectivamente. En Win32, todos los controladores son enteros de 32 bits. Sin embargo, cuando **se diseñó XLOPER,** Windows era un sistema de 16 bits. Por lo tanto, la estructura solo permite controladores de 16 bits. En Win32, cuando se llama con **Excel4** o **Excel4v,** la función **xlGetInst** y la función **xlGetHwnd** devuelven solo la parte baja del controlador completo de 32 bits. 
  
En Excel 2007 y versiones posteriores, cuando se llama a estas funciones con [Excel12](excel4-excel12.md) o [Excel12v,](excel4v-excel12v.md)el **XLOPER12** devuelto contiene el controlador completo de 32 bits. 
  
Obtener el identificador de instancia completo es sencillo en cualquier versión de Excel, ya que se pasa a la **dll de** devolución de llamada de Windows , que se llama cuando se carga la DLL. Si registra este identificador de instancia en una variable global, nunca tendrá que llamar a la **función xlGetInst.** 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Obtener el controlador de Excel principal en Excel 2003 y versiones anteriores

Para obtener el controlador Excel principal en Excel 2003 y versiones anteriores de 32 bits, primero debe llamar a la función **xlGetHwnd** para obtener la palabra baja del controlador real. A continuación, debe iterar la lista de ventanas de nivel superior para buscar una coincidencia con la palabra baja devuelta. El siguiente código ilustra la técnica. 
  
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
  
[Desarrollar archivos XLL de Excel](developing-excel-xlls.md)

