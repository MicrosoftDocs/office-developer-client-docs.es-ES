---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- función debugprintf [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424801"
---
# <a name="debugprintf"></a>debugPrintf

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de biblioteca de marcos que escribe una cadena de bytes terminada en null en el depurador activo a través de la función **OutputDebugStringA** de Windows SDK . Si la aplicación no tiene ningún depurador, el depurador del sistema muestra la cadena. Si la aplicación no tiene ningún depurador y el depurador del sistema no está activo, **debugPrintf** no hace nada. 
  
Esta función no devuelve un valor.
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>Parámetros

 _lpFormat (LPSTR)_
  
Cadena de formato, que sigue la sintaxis y las reglas que se usan con la **función sprintf.** 
  
 _argumentos_
  
Cero o más argumentos para que coincidan con la cadena de formato.
  
## <a name="example"></a>Ejemplo

Esta función imprime una cadena para mostrar que se le ha pasado el control. El _DEBUG debe definirse antes de compilar o, de lo contrario, esta función no hace nada.
  
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

## <a name="see-also"></a>Consulte también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

