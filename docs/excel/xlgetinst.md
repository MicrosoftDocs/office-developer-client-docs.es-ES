---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- Función xlgetinst [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e113ddbf55e2b4651d578549802c44e2c6413a18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428133"
---
# <a name="xlgetinst"></a>xlGetInst

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve el identificador de instancia de la instancia de Microsoft Excel que actualmente llama a una DLL.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parámetros

Esta función no tiene argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

El identificador de instancia (**xltypeInt**) estará en el **campo val.w.** 
  
## <a name="remarks"></a>Comentarios

Esta función se puede usar para distinguir entre varias instancias en ejecución de Excel que llaman a la DLL.
  
Cuando se llama a esta función mediante [Excel4](excel4-excel12.md) o [Excel4v,](excel4v-excel12v.md)la variable de entero XLOPER devuelta es un int corto de 16 bits firmado. Esto solo es capaz de contener los 16 bits bajos del controlador de Windows de 32 bits. A partir de Excel 2007, la variable entera de **XLOPER12** es un int de 32 bits firmado y, por lo tanto, contiene todo el controlador, lo que elimina la necesidad de iterar todas las ventanas abiertas. 
  
> [!IMPORTANT]
> Si la **función xlGetInst** se usa con la versión de 64 bits de Microsoft Excel, se producirá un error en la función. Esto se debe a que el tipo de valor **xltypeInt** no es lo suficientemente ancho como para contener el controlador de 64 bits de longitud devuelto por Excel en este caso. Para este propósito, Excel 2010 introdujo una nueva función denominada [xlGetInstPtr](xlgetinstptr.md), que se ejecuta correctamente con las versiones de Excel de 32 bits y 64 bits. 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se compara la instancia de la última copia de Excel que la llamó con la copia actual de Excel que la llamó. Si son iguales, devuelve 1; si no es así, devuelve 0; si se produce un error en la función, devuelve -1.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a>Consulte también



[xlGetHwnd](xlgethwnd.md)
  
[xlGetInstPtr](xlgetinstptr.md)


[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

