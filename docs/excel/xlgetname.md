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
# <a name="xlgetname"></a>xlGetName

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve el nombre de archivo y ruta de acceso completo del archivo DLL en el formulario de una cadena.
  
```cs
Excel12(xlGetName, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve la ruta de acceso y nombre de archivo (**xltypeStr**). 
  
## <a name="example"></a>Ejemplo

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

## <a name="see-also"></a>Vea también

- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

