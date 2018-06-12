---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- función xlGetHwnd [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a22365d6c945aaa5995e2c519c757a1a7515655a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815749"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve el identificador de ventana de la ventana de Microsoft Excel de nivel superior.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Sintaxis

Esta función no tiene argumentos.
  
## <a name="property-valuereturn-value"></a>Propiedad valor y valor devuelto

Contiene el identificador de ventana (**xltypeInt**) en el campo **val.w** . 
  
## <a name="remarks"></a>Notas

Esta función es útil para la escritura de código de API de Windows.
  
Cuando se llama a esta función mediante [Excel4](excel4-excel12.md) o [Excel4v](excel4v-excel12v.md), la variable de tipo entero XLOPER devuelta es un entero con signo 16 bits corto. Este valor solo es capaz de contener los 16 bits inferiores del identificador de Windows de 32 bits. Para buscar el elemento alta, el código debe recorrer en iteración todas las ventanas abiertas busca una coincidencia con la parte baja. Iniciar en Excel 2007, la variable de entero de **XLOPER12** es un int de 32 bits con signo y, por tanto, contiene un controlador de todo, eliminando la necesidad de recorrer en iteración todas las ventanas abiertas. 
  
### <a name="example"></a>Ejemplo

Vea el código para la [función fShowDialog](fshowdialog.md) en `SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Ver también

- [xlGetInst](xlgetinst.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

