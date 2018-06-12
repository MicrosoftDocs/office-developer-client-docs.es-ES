---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- debugprintf (función) [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815523"
---
# <a name="debugprintf"></a>debugPrintf

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de biblioteca de Framework que escribe una cadena de bytes terminada en null en el depurador activo a través de la función de Windows SDK **OutputDebugStringA**. Si la aplicación no tiene ningún depurador, el depurador del sistema muestra la cadena. Si la aplicación no tiene ningún depurador y el depurador del sistema no está activo, **debugPrintf** no tiene ningún efecto. 
  
Esta función no devuelve un valor.
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>Sintaxis

 _lpFormat (LPSTR)_
  
La cadena de formato, que sigue la sintaxis y las reglas para el que se utiliza con la función **sprintf** . 
  
 _argumentos_
  
Cero o más argumentos para que coincida con la cadena de formato.
  
## <a name="example"></a>Ejemplo

Esta función imprime una cadena para mostrar que el control se ha pasado a ella. El indicador _DEBUG debe definirse antes de compilar, o bien esta función no tiene ningún efecto.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a>Ver también



[Funciones de la biblioteca de Framework](functions-in-the-framework-library.md)

