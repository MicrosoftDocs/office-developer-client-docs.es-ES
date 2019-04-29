---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- función xlset [Excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0912c1d40882933778d0df927ceb9de773063444
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404606"
---
# <a name="xlset"></a>xlSet

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Coloca los valores constantes en celdas o rangos muy rápido. Para obtener más información, vea "xlSet y libros con fórmulas de matriz" en [problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Parameters

_pxReference_ (**xltypeRef** o **xltypeSRef**)
  
Una referencia rectangular que describe la celda o celdas de destino. La referencia debe describir las celdas adyacentes, de modo que en una **xltypeRef** `val.mref.lpmref->count` debe establecerse en 1. 
  
_pxValue_
  
Valor o valores que se van a colocar en la celda o celdas. Si desea más información, vea la sección "Comentarios".
  
## <a name="remarks"></a>Comentarios

### <a name="pxvalue-argument"></a>argumento pxValue

_pxValue_ puede ser un valor o una matriz. Si es un valor, todo el rango de destino se rellena con ese valor. Si es una matriz (**xltypeMulti**), los elementos de la matriz se colocan en las ubicaciones correspondientes del rectángulo.
  
Si usa una matriz horizontal para el segundo argumento, se duplica para rellenar todo el rectángulo. Si usa una matriz vertical, se duplica a la derecha para rellenar todo el rectángulo. Si usa una matriz rectangular y es demasiado pequeña para el rango rectangular en el que desea colocarla, dicho intervalo se rellenará con **#N/a**s.
  
Si el rango de destino es menor que la matriz de origen, los valores se copian hasta los límites del intervalo de destino y se omiten los datos adicionales.
  
Para borrar un elemento del rectángulo de destino, use un elemento de matriz de tipo **xltypeNil** en la matriz de origen. Para borrar todo el rectángulo de destino, omita el segundo argumento. 
  
### <a name="restrictions"></a>Restringi

**xlSet** no se puede deshacer. Además, destruye la información de deshacer que puede haber estado disponible antes. 
  
**xlSet** puede incluir constantes, no fórmulas, en las celdas. 
  
**xlSet** se comporta como una función equivalente al comando de clase 3; es decir, solo está disponible dentro de un archivo DLL cuando se llama a la DLL desde un objeto, una macro, un menú, una barra de herramientas, una tecla de método abreviado o el botón **Ejecutar** en el cuadro de diálogo **macro** (al que se tiene acceso desde la ficha **Ver** de la cinta de opción a partir de Excel 2007 y las **herramientas **menú de versiones anteriores). 
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo rellena B205: B206 con el valor que se pasó desde una macro. Este ejemplo de función de comando requiere un argumento, por lo que sólo funcionará si se llama desde una hoja de macros XLM, o desde un módulo de VBA mediante el método **Application. Run** . 
  
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

## <a name="see-also"></a>Ver también

- [xlCoerce](xlcoerce.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

