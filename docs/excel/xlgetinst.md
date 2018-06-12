---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- xlgetinst (función) [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9484f7bbc1f5e0fc5b0def17f2ce79ef226dcd17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815736"
---
# <a name="xlgetinst"></a>xlGetInst

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve el identificador de instancia de la instancia de Microsoft Excel que actualmente se está llamando a un archivo DLL.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Sintaxis

Esta función no tiene argumentos.
  
## <a name="property-valuereturn-value"></a>Propiedad valor y valor devuelto

El identificador de instancia (**xltypeInt**) estará en el campo **val.w** . 
  
## <a name="remarks"></a>Notas

Esta función puede usarse para distinguir entre varias instancias en ejecución de Excel que se va a llamar a la DLL.
  
Cuando se llama a esta función mediante [Excel4](excel4-excel12.md) o [Excel4v](excel4v-excel12v.md), la variable de tipo entero XLOPER devuelta es un entero con signo 16 bits corto. Este valor solo es capaz de contener los 16 bits inferiores del identificador de Windows de 32 bits. Iniciar en Excel 2007, la variable de entero de **XLOPER12** es un int de 32 bits con signo y, por tanto, contiene un controlador de todo, eliminando la necesidad de recorrer en iteración todas las ventanas abiertas. 
  
> [!IMPORTANT]
> Si se usa la función **xlGetInst** con la versión de 64 bits de Microsoft Excel, se producirá un error en la función. Esto es debido a que el tipo de valor **xltypeInt** no es lo suficientemente ancho como para contener el identificador de tipo long de 64 bits devuelto por Excel en este caso. Para este propósito, Excel 2010 introdujo una nueva función denominada [xlGetInstPtr](xlgetinstptr.md), que se ejecuta correctamente con las versiones de 32 bits y 64 bits de Excel. 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se compara la instancia de la última copia de Excel que llama a la copia actual de Excel que lo llamó. Si son iguales, devuelve 1; en caso contrario, devuelve 0; Si se produce un error en la función, devuelve -1.
  
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

## <a name="see-also"></a>Ver también



[xlGetHwnd](xlgethwnd.md)
  
[xlGetInstPtr](xlgetinstptr.md)


[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

