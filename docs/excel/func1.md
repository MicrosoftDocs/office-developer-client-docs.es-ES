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
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408918"
---
# <a name="func1"></a>Func1

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
La función de hoja de cálculo definida por el usuario muestra el retorno de un valor de cadena estática. Cuando se carga GENERIC.xll, registra esta función para que se pueda llamar desde la hoja de cálculo.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Parameters

 _px_ (**LPXLOPER**)
  
Este argumento se omite y solo sirve para desencadenar Microsoft Excel llamar a la función.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

 **LPXLOPER12**: Siempre la cadena "Func1"
  
### <a name="example"></a>Ejemplo

Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

