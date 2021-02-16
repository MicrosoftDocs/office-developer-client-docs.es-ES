---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- función tempstr12 [excel 2007],Función TempStrConst [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d93f9de021c7ba325d9c11af2cede0245ffbbf6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407154"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de biblioteca de marcos que crea un **XLOPER/XLOPER12** temporal que contiene una cadena **xltypeStr,** tomando una cadena de origen terminada en null como entrada. La función asigna un nuevo búfer de memoria y copia la cadena pasada en él. La cadena de entrada no se modifica y, por lo tanto, se declara **como constante**.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Parámetros

 _str_
  
Puntero a la cadena de origen terminada en null. En el caso de **XLOPER,** TempStrConst trunca cadenas que tienen más de 255 bytes. En el caso de **XLOPER12,** TempStr12Const trunca cadenas que tienen más de 32.767 caracteres Unicode.
  
## <a name="return-value"></a>Valor devuelto

Devuelve una **cadena xltypeStr** que contiene una copia del búfer de cadena pasado. 
  
## <a name="remarks"></a>Comentarios

Tenga en cuenta que la función marco de cadena **XLOPER,** **TempStr**, se comporta de forma diferente e intenta sobrescribir el primer carácter de la cadena proporcionada con la longitud de la cadena posterior. Esto no siempre es algo seguro: Microsoft Excel podría bloquearse si se pasa una cadena de solo lectura. Esta forma de crear cadenas temporales ahora está en desuso en favor de la forma en que funcionan **tanto TempStrConst** como **TempStr12.** Por lo tanto, el primer carácter de la cadena de entrada se trata como el inicio de la cadena, es decir, no como un carácter de longitud o como un espacio para un carácter de longitud. No debes pasar cadenas que tengan un carácter de longitud codificado al principio, ya que las consecuencias podrían ser impredecibles. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se usa **la función TempStr12** para crear una cadena para un cuadro de mensaje. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a>Consulte también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

