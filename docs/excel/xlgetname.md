---
title: xlGetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetName
keywords:
- función xlgetname [Excel 2007]
localization_priority: Normal
ms.assetid: 72dbebc0-7436-4771-8fbf-2b445341da65
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 350ae99baf088a36fa3e1159caa1805cdd623276
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303832"
---
# <a name="xlgetname"></a><span data-ttu-id="a2196-104">xlGetName</span><span class="sxs-lookup"><span data-stu-id="a2196-104">xlGetName</span></span>

<span data-ttu-id="a2196-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a2196-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a2196-106">Devuelve la ruta de acceso completa y el nombre de archivo de la DLL en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="a2196-106">Returns the full path and file name of the DLL in the form of a string.</span></span>
  
```cs
Excel12(xlGetName, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="a2196-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="a2196-107">Parameters</span></span>

<span data-ttu-id="a2196-108">Esta función no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="a2196-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a2196-109">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2196-109">Property value/Return value</span></span>

<span data-ttu-id="a2196-110">Devuelve la ruta de acceso y el nombre de archivo (**xltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="a2196-110">Returns the path and file name (**xltypeStr**).</span></span> 
  
## <a name="example"></a><span data-ttu-id="a2196-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2196-111">Example</span></span>

`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetNameExample(void)
{
    XLOPER12 xRes;
    Excel12(xlGetName, (LPXLOPER12)&xRes, 0);
    Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a2196-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2196-112">See also</span></span>

- [<span data-ttu-id="a2196-113">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="a2196-113">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

