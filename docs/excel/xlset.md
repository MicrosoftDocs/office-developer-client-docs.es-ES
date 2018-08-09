---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- función xlSet [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 63f50e441f5d851677f36754a17bcd6403705239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815755"
---
# <a name="xlset"></a>xlSet

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Coloca los valores de constantes en las celdas o rangos de muy rápidamente. Para obtener más información, consulte "xlSet y libros con fórmulas de matriz" de [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Parámetros

_pxReference_ (**xltypeRef** o **xltypeSRef**)
  
Una referencia rectangular que describe la celda de destino o celdas. La referencia debe describir las celdas adyacentes, por lo que en un **xltypeRef** `val.mref.lpmref->count` se debe establecer en 1. 
  
_pxValue_
  
El valor o los valores que desea colocar en la celda o celdas. Para obtener más información, vea la sección "Comentarios".
  
## <a name="remarks"></a>Comentarios

### <a name="pxvalue-argument"></a>argumento de pxValue

_pxValue_ puede ser un valor o una matriz. Si es un valor, el rango de destino completo se rellena con ese valor. Si es una matriz (**xltypeMulti**), los elementos de la matriz se colocan en las ubicaciones correspondientes en el rectángulo.
  
Si utiliza una matriz horizontal para el segundo argumento, se duplican hacia abajo para rellenar todo el rectángulo. Si utiliza una matriz vertical, se duplican a la derecha para rellenar todo el rectángulo. Si utiliza una matriz rectangular y es demasiado pequeño para el rango rectangular que desea colocar en, dicho rango se rellena con s **# N/a**.
  
Si el rango de destino es menor que la matriz de origen, los valores se copian en hasta los límites del rango de destino y se omiten los datos adicionales.
  
Para borrar un elemento del rectángulo de destino, use un elemento de matriz de tipo de **xltypeNil** en la matriz de origen. Para borrar el rectángulo de destino completa, omite el segundo argumento. 
  
### <a name="restrictions"></a>Restricciones

**xlSet** no se puede deshacer. Además, destruye cualquier información de deshacer que puede haber sido antes. 
  
**xlSet** puede colocar sólo las constantes, no fórmulas, en las celdas. 
  
**xlSet** se comporta como una función de comando equivalente de la clase 3; es decir, está disponible sólo dentro de un archivo DLL cuando se llama a la DLL desde un objeto, macro, menú, la barra de herramientas, teclas de método abreviado o el botón **Ejecutar** en el cuadro de diálogo **Macro** (obtener acceso desde la ficha de **vista** de la cinta de opciones a partir de Excel 2007 y las herramientas de ** **menú en las versiones anteriores). 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se rellena B205:B206 con el valor que se pasó desde una macro. En este ejemplo de la función comando requiere un argumento por lo que sólo funcionará si se le llama desde una hoja de macros XLM, o desde un módulo de VBA mediante el método **Application.Run** . 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a>Vea también

- [xlCoerce](xlcoerce.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

