---
title: Funciones de la biblioteca de marcos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- funciones de la biblioteca de marcos [Excel 2007], funciones [Excel 2007], biblioteca de marcos
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417549"
---
# <a name="functions-in-the-framework-library"></a>Funciones de la biblioteca de marcos

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
La biblioteca de .NET Framework se creó para facilitar la escritura de XLL. Incluye funciones sencillas para la administración de la memoria**xloper12** de **XLOPER**/ , la creación de **XLOPER**/ **xloper12**temporal, la llamada sólida a las funciones de devolución de llamada de Microsoft Excel (**Excel4**, **Excel4v** , * * Excel12 * *, * * Excel12v * *) e imprimir cadenas de depuración en un terminal adjunto.
  
Las funciones incluidas en esta biblioteca ayudan a simplificar una parte del código similar a la siguiente.
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

El código simplificado es similar al ejemplo siguiente.
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

Las siguientes funciones se incluyen en la biblioteca de Framework:
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**GetTempMemory** <br/> |
|**FreeAllTempMemory** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**Funciones utilizadas con XLOPER**|**Funciones utilizadas con Xloper12**|
|:-----|:-----|
|[Excel](excel-excel12f.md) <br/> |[Excel12f](excel-excel12f.md) <br/> |
|[TempNum](tempnum-tempnum12.md) <br/> |[TempNum12](tempnum-tempnum12.md) <br/> |
|[TempStr](tempstr.md) <br/> |[TempStr12](tempstrconst-tempstr12.md) <br/> |
|[TempStrConst](tempstrconst-tempstr12.md) <br/> |[TempStr12Const](tempstrconst-tempstr12.md) <br/> |
|[TempBool](tempbool-tempbool12.md) <br/> |[TempBool12](tempbool-tempbool12.md) <br/> |
|[TempInt](tempint-tempint12.md) <br/> |[TempInt12](tempint-tempint12.md) <br/> |
|[Templating](temperr-temperr12.md) <br/> |[TempErr12](temperr-temperr12.md) <br/> |
|[TempActiveRef](tempactiveref-tempactiveref12.md) <br/> |[TempActiveRef12](tempactiveref-tempactiveref12.md) <br/> |
|[TempActiveCell](tempactivecell-tempactivecell12.md) <br/> |[TempActiveCell12](tempactivecell-tempactivecell12.md) <br/> |
|[TempActiveRow](tempactiverow-tempactiverow12.md) <br/> |[TempActiveRow12](tempactiverow-tempactiverow12.md) <br/> |
|[TempActiveColumn](tempactivecolumn-tempactivecolumn12.md) <br/> |[TempActiveColumn12](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[TempMissing](tempmissing-tempmissing12.md) <br/> |[TempMissing12](tempmissing-tempmissing12.md) <br/> |
   
El uso de estas funciones reduce la cantidad de tiempo necesario para escribir una DLL o XLL. Si se inicia el desarrollo a partir de la aplicación de muestra genérica también se reduce el tiempo de desarrollo. Usar GENERIC. C como plantilla para ayudar a configurar el marco de un XLL y, a continuación, reemplace el código existente por el suyo propio.
  
Las funciones de**xloper12** de **XLOPER**/ temporales crean valores **XLOPER**/ **xloper12** mediante la memoria de un montón local administrado por la biblioteca de Framework. Los valores de**XLOPER12** de **XLOPER**/ siguen siendo válidos hasta que se llama a la función **FreeAllTempMemory** o a cualquiera de las funciones **Excel** o **Excel12f** . (Las funciones **Excel** y **Excel12f** liberan toda la memoria temporal antes de devolverse). 
  
Para usar las funciones de la biblioteca de Marcos, debe incluir FRAMEWRK. H en el código C y agregue FRAMEWRK. C o FRMWRK32. LIB a su proyecto de código.
  
## <a name="see-also"></a>Ver también

- [Referencia de funciones de API de SDK de XLL de Excel 2013](excel-xll-sdk-api-function-reference.md)

