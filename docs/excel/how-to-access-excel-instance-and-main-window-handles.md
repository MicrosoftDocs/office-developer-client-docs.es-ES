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
ms.openlocfilehash: 4b71ccd428e60c9ba2e59fea0e56eb2fc61390db
ms.sourcegitcommit: 4590b7ed906d008693a58abe63f089ed8a380b34
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2018
ms.locfileid: "26643181"
---
# <a name="access-excel-instance-and-main-window-handles"></a><span data-ttu-id="5c631-104">Obtener acceso a la instancia de Excel y los controladores de la ventana principal</span><span class="sxs-lookup"><span data-stu-id="5c631-104">Access Excel Instance and Main Window Handles</span></span>

 <span data-ttu-id="5c631-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5c631-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5c631-106">A veces para programar en el entorno de Windows, debe conocer el identificador de la instancia de Microsoft Excel o la ventana principal de administrar.</span><span class="sxs-lookup"><span data-stu-id="5c631-106">To program in the Windows environment, sometimes you must know the Microsoft Excel instance handle or main window handle.</span></span> <span data-ttu-id="5c631-107">Por ejemplo, estos controladores son útiles cuando se están creando y mostrar cuadros de diálogo de Windows personalizados.</span><span class="sxs-lookup"><span data-stu-id="5c631-107">For example, these handles are useful when you are creating and displaying custom Windows dialog boxes.</span></span>
  
<span data-ttu-id="5c631-108">Hay dos funciones de la API de C sólo XLL que proporcionan acceso a estos controladores: la función [xlGetInst](xlgetinst.md) y la [xlGetHwnd](xlgethwnd.md) funcionan respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5c631-108">There are two XLL-only C API functions that provide access to these handles: the [xlGetInst](xlgetinst.md) function and the [xlGetHwnd](xlgethwnd.md) function respectively.</span></span> <span data-ttu-id="5c631-109">En Win32, todos los identificadores son números enteros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5c631-109">In Win32, all handles are 32-bit integers.</span></span> <span data-ttu-id="5c631-110">Sin embargo, cuando se diseñó el **XLOPER** , Windows era un sistema de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5c631-110">However, when the **XLOPER** was designed, Windows was a 16-bit system.</span></span> <span data-ttu-id="5c631-111">Por lo tanto, la estructura que sólo se permite para controladores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5c631-111">Therefore, the structure only allowed for 16-bit handles.</span></span> <span data-ttu-id="5c631-112">En Win32, cuando se llama con **Excel4** o **Excel4v**, la función **xlGetInst** y la función **xlGetHwnd** devuelven sólo la parte baja del identificador de 32 bits completa.</span><span class="sxs-lookup"><span data-stu-id="5c631-112">In Win32, when called with **Excel4** or **Excel4v**, the **xlGetInst** function and the **xlGetHwnd** function return only the low part of the full 32-bit handle.</span></span> 
  
<span data-ttu-id="5c631-113">En Excel 2007 y versiones posteriores, cuando se llaman a estas funciones con [Excel12](excel4-excel12.md) o [Excel12v](excel4v-excel12v.md), **XLOPER12** devuelto contiene un controlador de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5c631-113">In Excel 2007 and later versions, when these functions are called with [Excel12](excel4-excel12.md) or [Excel12v](excel4v-excel12v.md), the returned **XLOPER12** contains the full 32-bit handle.</span></span> 
  
<span data-ttu-id="5c631-114">Obtener el identificador de instancia completa es simple en cualquier versión de Excel, tal como se pasa a la devolución de llamada de Windows **DllMain**, que se llama cuando se carga el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="5c631-114">Obtaining the full instance handle is simple in any version of Excel, as it is passed to the Windows callback **DllMain**, which is called when the DLL is loaded.</span></span> <span data-ttu-id="5c631-115">Si registrar este identificador de instancia en una variable global, nunca debe llamar a la función **xlGetInst** .</span><span class="sxs-lookup"><span data-stu-id="5c631-115">If you record this instance handle in a global variable, you never need to call the **xlGetInst** function.</span></span> 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a><span data-ttu-id="5c631-116">Obtener el identificador principal de Excel en Excel 2003 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="5c631-116">Obtaining the Main Excel Handle in Excel 2003 and Earlier</span></span>

<span data-ttu-id="5c631-117">Para obtener el identificador principal de Excel en Excel 2003 y versiones anteriores de 32 bits, primero debe llamar a la función **xlGetHwnd** para obtener la palabra baja del identificador real.</span><span class="sxs-lookup"><span data-stu-id="5c631-117">To obtain the main Excel handle in Excel 2003 and earlier 32-bit versions, you must first call the **xlGetHwnd** function to obtain the low word of the actual handle.</span></span> <span data-ttu-id="5c631-118">A continuación, debe recorrer en iteración la lista de ventanas de nivel superior para buscar una coincidencia con la palabra baja devuelta.</span><span class="sxs-lookup"><span data-stu-id="5c631-118">Then, you must iterate the list of top-level windows to search for a match with the returned low word.</span></span> <span data-ttu-id="5c631-119">El siguiente código muestra la técnica.</span><span class="sxs-lookup"><span data-stu-id="5c631-119">The following code illustrates the technique.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="5c631-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c631-120">See also</span></span>



[<span data-ttu-id="5c631-121">Mostrar cuadros de diálogo desde dentro de una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="5c631-121">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[<span data-ttu-id="5c631-122">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="5c631-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="5c631-123">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="5c631-123">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

