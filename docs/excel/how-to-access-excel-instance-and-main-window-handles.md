---
title: Obtener acceso a identificadores de instancia de Excel y ventana principal
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- obtener acceso a controladores de Excel,handles [Excel 2007], accessing,Excel instances, accessing,window handles [Excel 2007], accessing
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
# <a name="access-excel-instance-and-main-window-handles"></a><span data-ttu-id="aa029-104">Obtener acceso a identificadores de instancia de Excel y ventana principal</span><span class="sxs-lookup"><span data-stu-id="aa029-104">Access Excel Instance and Main Window Handles</span></span>

 <span data-ttu-id="aa029-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="aa029-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="aa029-106">Para programar en el entorno de Windows, a veces debe conocer el identificador de instancia de Microsoft Excel o el controlador de la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="aa029-106">To program in the Windows environment, sometimes you must know the Microsoft Excel instance handle or main window handle.</span></span> <span data-ttu-id="aa029-107">Por ejemplo, estos controladores son útiles al crear y mostrar cuadros de diálogo personalizados de Windows.</span><span class="sxs-lookup"><span data-stu-id="aa029-107">For example, these handles are useful when you are creating and displaying custom Windows dialog boxes.</span></span>
  
<span data-ttu-id="aa029-108">Hay dos funciones de la API de C solo XLL que proporcionan acceso a estos controladores: la función [xlGetInst](xlgetinst.md) y la función [xlGetHwnd](xlgethwnd.md) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="aa029-108">There are two XLL-only C API functions that provide access to these handles: the [xlGetInst](xlgetinst.md) function and the [xlGetHwnd](xlgethwnd.md) function respectively.</span></span> <span data-ttu-id="aa029-109">En Win32, todos los controladores son enteros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="aa029-109">In Win32, all handles are 32-bit integers.</span></span> <span data-ttu-id="aa029-110">Sin embargo, cuando **se diseñó XLOPER,** Windows era un sistema de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="aa029-110">However, when the **XLOPER** was designed, Windows was a 16-bit system.</span></span> <span data-ttu-id="aa029-111">Por lo tanto, la estructura solo permite controladores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="aa029-111">Therefore, the structure only allowed for 16-bit handles.</span></span> <span data-ttu-id="aa029-112">En Win32, cuando se llama con **Excel4** o **Excel4v,** la función **xlGetInst** y la función **xlGetHwnd** devuelven solo la parte baja del controlador de 32 bits completo.</span><span class="sxs-lookup"><span data-stu-id="aa029-112">In Win32, when called with **Excel4** or **Excel4v**, the **xlGetInst** function and the **xlGetHwnd** function return only the low part of the full 32-bit handle.</span></span> 
  
<span data-ttu-id="aa029-113">En Excel 2007 y versiones posteriores, cuando se llama a estas funciones con [Excel12](excel4-excel12.md) o [Excel12v,](excel4v-excel12v.md)el **XLOPER12** devuelto contiene el controlador completo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="aa029-113">In Excel 2007 and later versions, when these functions are called with [Excel12](excel4-excel12.md) or [Excel12v](excel4v-excel12v.md), the returned **XLOPER12** contains the full 32-bit handle.</span></span> 
  
<span data-ttu-id="aa029-114">Obtener el identificador de instancia completo es sencillo en cualquier versión de Excel, ya que se pasa a la **dllMain** de devolución de llamada de Windows, que se llama cuando se carga la DLL.</span><span class="sxs-lookup"><span data-stu-id="aa029-114">Obtaining the full instance handle is simple in any version of Excel, as it is passed to the Windows callback **DllMain**, which is called when the DLL is loaded.</span></span> <span data-ttu-id="aa029-115">Si registra este identificador de instancia en una variable global, nunca tendrá que llamar a la **función xlGetInst.**</span><span class="sxs-lookup"><span data-stu-id="aa029-115">If you record this instance handle in a global variable, you never need to call the **xlGetInst** function.</span></span> 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a><span data-ttu-id="aa029-116">Obtener el controlador principal de Excel en Excel 2003 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="aa029-116">Obtaining the Main Excel Handle in Excel 2003 and Earlier</span></span>

<span data-ttu-id="aa029-117">Para obtener el controlador principal de Excel en Excel 2003 y versiones anteriores de 32 bits, primero debe llamar a la función **xlGetHwnd** para obtener la palabra baja del identificador real.</span><span class="sxs-lookup"><span data-stu-id="aa029-117">To obtain the main Excel handle in Excel 2003 and earlier 32-bit versions, you must first call the **xlGetHwnd** function to obtain the low word of the actual handle.</span></span> <span data-ttu-id="aa029-118">A continuación, debe iterar la lista de ventanas de nivel superior para buscar una coincidencia con la palabra baja devuelta.</span><span class="sxs-lookup"><span data-stu-id="aa029-118">Then, you must iterate the list of top-level windows to search for a match with the returned low word.</span></span> <span data-ttu-id="aa029-119">El siguiente código ilustra la técnica.</span><span class="sxs-lookup"><span data-stu-id="aa029-119">The following code illustrates the technique.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="aa029-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aa029-120">See also</span></span>



[<span data-ttu-id="aa029-121">Mostrar cuadros de diálogo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="aa029-121">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[<span data-ttu-id="aa029-122">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="aa029-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="aa029-123">Desarrollar archivos XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="aa029-123">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

