---
title: Funciones de la biblioteca de marcos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- funciones de la biblioteca Framework [excel 2007], [Excel 2007], funciones de biblioteca de Framework
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815647"
---
# <a name="functions-in-the-framework-library"></a>Funciones de la biblioteca de marcos

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
La biblioteca de Framework se creó para facilitar la escritura de los XLL sea más fáciles. Incluye funciones simples para la gestión **XLOPER**/ memoria**XLOPER12** , creación temporal **XLOPER**/ **XLOPER12**, con solidez al llamar a las funciones de devolución de llamada de Microsoft Excel (**Excel4**, **Excel4v** ** Excel12 **, ** Excel12v **) y la impresión de depuración de cadenas en un terminal adjunto.
  
Las funciones incluidas en esta biblioteca ayudan a simplificar un fragmento de código que es similar a la siguiente.
  
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

En la biblioteca de Framework se incluyen las funciones siguientes:
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**GetTempMemory** <br/> |
|**FreeAllTempMemory** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**Funciones usadas con XLOPER**|**Funciones usadas con XLOPER12s**|
|:-----|:-----|
|[Excel](excel-excel12f.md) <br/> |[Excel12f](excel-excel12f.md) <br/> |
|[TempNum](tempnum-tempnum12.md) <br/> |[TempNum12](tempnum-tempnum12.md) <br/> |
|[TempStr](tempstr.md) <br/> |[TempStr12](tempstrconst-tempstr12.md) <br/> |
|[TempStrConst](tempstrconst-tempstr12.md) <br/> |[TempStr12Const](tempstrconst-tempstr12.md) <br/> |
|[TempBool](tempbool-tempbool12.md) <br/> |[TempBool12](tempbool-tempbool12.md) <br/> |
|[TempInt](tempint-tempint12.md) <br/> |[TempInt12](tempint-tempint12.md) <br/> |
|[TempErr](temperr-temperr12.md) <br/> |[TempErr12](temperr-temperr12.md) <br/> |
|[TempActiveRef](tempactiveref-tempactiveref12.md) <br/> |[TempActiveRef12](tempactiveref-tempactiveref12.md) <br/> |
|[TempActiveCell](tempactivecell-tempactivecell12.md) <br/> |[TempActiveCell12](tempactivecell-tempactivecell12.md) <br/> |
|[TempActiveRow](tempactiverow-tempactiverow12.md) <br/> |[TempActiveRow12](tempactiverow-tempactiverow12.md) <br/> |
|[TempActiveColumn](tempactivecolumn-tempactivecolumn12.md) <br/> |[TempActiveColumn12](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[TempMissing](tempmissing-tempmissing12.md) <br/> |[TempMissing12](tempmissing-tempmissing12.md) <br/> |
   
Uso de estas funciones reduce la cantidad de tiempo necesaria para escribir una DLL o XLL. Iniciar el desarrollo de la aplicación de ejemplo genérico también reduce el tiempo de desarrollo. Use genérico. C como una plantilla para ayudar a configurar el marco de trabajo de un XLL y, a continuación, reemplace el código existente por el suyo propio.
  
El temporal **XLOPER**/ **XLOPER12** funciones creación **XLOPER**/ **XLOPER12** valores mediante el uso de memoria de un montón local administrado por la biblioteca de Framework. El **XLOPER**/ **XLOPER12** valores permanecen válidos hasta que se llame a la función **FreeAllTempMemory** o cualquiera de las funciones de **Excel** o **Excel12f** . (Las funciones de **Excel** y **Excel12f** gratuita de toda la memoria temporal antes de devolver). 
  
Para usar las funciones de la biblioteca de Framework, debe incluir el FRAMEWRK. Según se trate de archivos en el código de C y agregar la FRAMEWRK. C o FRMWRK32. Archivos de LIB a su proyecto de código.
  
## <a name="see-also"></a>Vea también

- [Referencia de funciones de API de SDK de XLL de Excel 2013](excel-xll-sdk-api-function-reference.md)

