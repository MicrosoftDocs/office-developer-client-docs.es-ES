---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- función xlgethwnd [Excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425459"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve el controlador de la ventana de Microsoft Excel de nivel superior.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parameters

Esta función no tiene argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Contiene el identificador de ventana (**xltypeInt**) en el campo **Val. w** . 
  
## <a name="remarks"></a>Comentarios

Esta función es útil para escribir código de API de Windows.
  
Cuando se llama a esta función mediante [Excel4](excel4-excel12.md) o [Excel4v](excel4v-excel12v.md), la variable de entero del XLOPER que se devuelve es un int Short de 16 bits firmado. Esto solo puede contener los 16 bits bajos del controlador de Windows de 32 bits. Para encontrar la parte alta, el código debe recorrer en iteración todas las ventanas abiertas que busquen una coincidencia con la parte baja. A partir de Excel 2007, la variable de entero de **XLOPER12** es un int de 32 bits firmado y, por lo tanto, contiene todo el identificador, lo que elimina la necesidad de recorrer en iteración todas las ventanas abiertas. 
  
### <a name="example"></a>Ejemplo

Consulte el código de la [función fShowDialog](fshowdialog.md) en `SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Ver también

- [xlGetInst](xlgetinst.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

