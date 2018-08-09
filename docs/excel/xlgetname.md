---
title: xlGetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetName
keywords:
- xlgetname (función) [excel 2007]
localization_priority: Normal
ms.assetid: 72dbebc0-7436-4771-8fbf-2b445341da65
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 069676957d280a0bf3b398bb23b27f0e654bc655
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815733"
---
# <a name="xlgetname"></a><span data-ttu-id="fe842-104">xlGetName</span><span class="sxs-lookup"><span data-stu-id="fe842-104">xlGetName</span></span>

<span data-ttu-id="fe842-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fe842-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fe842-106">Devuelve el nombre de archivo y ruta de acceso completo del archivo DLL en el formulario de una cadena.</span><span class="sxs-lookup"><span data-stu-id="fe842-106">Returns the full path and file name of the DLL in the form of a string.</span></span>
  
```cs
Excel12(xlGetName, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="fe842-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe842-107">Parameters</span></span>

<span data-ttu-id="fe842-108">Esta función no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="fe842-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="fe842-109">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe842-109">Property value/Return value</span></span>

<span data-ttu-id="fe842-110">Devuelve la ruta de acceso y nombre de archivo (**xltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="fe842-110">Returns the path and file name (**xltypeStr**).</span></span> 
  
## <a name="example"></a><span data-ttu-id="fe842-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe842-111">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="fe842-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe842-112">See also</span></span>

- [<span data-ttu-id="fe842-113">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="fe842-113">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

