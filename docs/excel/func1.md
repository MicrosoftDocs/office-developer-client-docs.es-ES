---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- función func1 [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 26439f1fb05aae2077844ce19935d9ff99e4f701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815634"
---
# <a name="func1"></a>Func1

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de hoja de cálculo definida por el usuario de ejemplo muestra la devolución de un valor de cadena estática. Cuando se carga GENERIC.xll, registra esta función para que se pueda llamar desde la hoja de cálculo.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Parámetros

 _px_ (**LPXLOPER**)
  
Este argumento se omite y sólo sirve para Microsoft Excel para llamar a la función de desencadenador.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

 **LPXLOPER12**: siempre la cadena "Func1"
  
### <a name="example"></a>Ejemplo

Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones de la DLL genérica](functions-in-the-generic-dll.md)

