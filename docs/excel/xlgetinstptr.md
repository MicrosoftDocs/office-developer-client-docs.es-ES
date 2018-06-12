---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815748"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve el identificador de instancia de la instancia de Microsoft Excel que actualmente se está llamando a un archivo DLL.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Sintaxis

Esta función no tiene argumentos.
  
## <a name="property-valuereturn-value"></a>Propiedad valor y valor devuelto

El identificador de instancia (**xltypeBigData**) estará en el campo **val.bigdata.h.hdata** . 
  
## <a name="remarks"></a>Notas

Esta función puede usarse para distinguir entre varias instancias en ejecución de Excel que se va a llamar a la DLL.
  
Esta función devuelve un valor correcto con las versiones de 32 bits y 64 bits de Excel. Se introdujo en Excel 2010, como una extensión a la función [xlGetInst](xlgetinst.md) , que funciona correctamente sólo con las versiones de 32 bits de Excel. 
  
Esta función funciona correctamente cuando se llama mediante el uso de las variedades [Excel4 y Excel12](excel4-excel12.md) de las funciones de devolución de llamada de API, porque **XLOPER** y **XLOPER12** tienen la misma estructura que admite el valor **xltypeBigData** Escriba. 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se compara la instancia de la última copia de Excel que llama a la copia actual de Excel que lo llamó. Si son iguales, devuelve 1; en caso contrario, devuelve 0; Si se produce un error en la función, devuelve -1. Este ejemplo funciona con versiones de 32 bits y 64 bits de Excel.
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
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

- [xlGetHwnd](xlgethwnd.md)
- [xlGetInst](xlgetinst.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

