---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fd4b4ad5bf52f29384ef7e0ba738c350189f471e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405285"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve el identificador de instancia de la instancia de Microsoft Excel que actualmente llama a un archivo DLL.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameters

Esta función no tiene argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

El identificador de instancia (**xltypeBigData**) estará en el **campo val.bigdata.h.hdata.** 
  
## <a name="remarks"></a>Comentarios

Esta función se puede usar para distinguir entre varias instancias en ejecución de Excel que llaman a la DLL.
  
Esta función devuelve un valor correcto con versiones de 32 bits y 64 bits de Excel. Se introdujo en Excel 2010 como una extensión de la función [xlGetInst,](xlgetinst.md) que funciona correctamente solo con versiones de 32 bits de Excel. 
  
Esta función funciona correctamente cuando se llama mediante las variedades Excel4 y [Excel12](excel4-excel12.md) de las funciones de devolución de llamada api, ya que **tanto XLOPER** como **XLOPER12** tienen la misma estructura que admite el tipo de valor **xltypeBigData.** 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se compara la instancia de la última copia de Excel que la llamó a la copia actual de Excel que la llamó. Si son iguales, devuelve 1; si no es así, devuelve 0; si se produce un error en la función, devuelve -1. Este ejemplo funciona con versiones de 32 bits y 64 bits de Excel.
  
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

## <a name="see-also"></a>Vea también

- [xlGetHwnd](xlgethwnd.md)
- [xlGetInst](xlgetinst.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

