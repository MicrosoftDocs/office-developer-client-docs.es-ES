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
- tempstr12 (función) [excel 2007], TempStrConst (función) [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815712"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Función de la biblioteca de Framework que crea un temporal **XLOPER y XLOPER12** que contiene una cadena **xltypeStr** , tomando una cadena terminada en null de origen como entrada. La función asigna un nuevo búfer de memoria y copia la cadena que se pasan en él. La cadena de entrada no se ha modificado y por lo que se declara como **const**.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Sintaxis

 _str_
  
Un puntero a la cadena de origen terminada en null. En el caso de s **XLOPER**, TempStrConst trunca cadenas que son mayores de 255 bytes. En el caso de s **XLOPER12**, TempStr12Const trunca cadenas que son más de 32.767 caracteres Unicode.
  
## <a name="return-value"></a>Valor devuelto

Devuelve una cadena de **xltypeStr** que contiene una copia del búfer se pasan en la cadena. 
  
## <a name="remarks"></a>Notas

Tenga en cuenta que la cadena **XLOPER** función Framework, **TempStr**, se comporta de manera diferente e intenta sobrescribir el primer carácter de la cadena proporcionada con la longitud de cadena subsiguientes. No siempre es algo seguro: Microsoft Excel podría bloquearse si se pasa una cadena de sólo lectura. Este modo de creación de cadenas temporales ahora está en desuso en favor de la manera en que trabajan **TempStrConst** y **TempStr12** . Por lo tanto, el primer carácter de la cadena de entrada se trata como el inicio de la cadena, es decir, no como un carácter de longitud o como un espacio para un carácter de longitud. No debe pasar las cadenas que tienen un carácter de longitud codificado al principio, como las consecuencias podrían ser impredecibles. 
  
## <a name="example"></a>Ejemplo

En este ejemplo se usa la función **TempStr12** para crear una cadena de un cuadro de mensaje. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a>Ver también



[Funciones de la biblioteca de Framework](functions-in-the-framework-library.md)

