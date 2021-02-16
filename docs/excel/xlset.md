---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- función xlset [excel 2007]
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
  
Coloca valores constantes en celdas o rangos muy rápidamente. Para obtener más información, vea "xlSet y libros con fórmulas de matriz" en Problemas conocidos en el desarrollo [de XLL de Excel.](known-issues-in-excel-xll-development.md)
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Parámetros

_pxReference_ (**xltypeRef** o **xltypeSRef**)
  
Referencia rectangular que describe la celda o celdas de destino. La referencia debe describir las celdas adyacentes, de modo que en **un xltypeRef** `val.mref.lpmref->count` debe establecerse en 1. 
  
_pxValue_
  
Valor o valores que se colocarán en la celda o celdas. Si desea más información, vea la sección "Comentarios".
  
## <a name="remarks"></a>Comentarios

### <a name="pxvalue-argument"></a>argumento pxValue

_pxValue_ puede ser un valor o una matriz. Si es un valor, todo el intervalo de destino se rellena con ese valor. Si se trata de una matriz (**xltypeMulti**), los elementos de la matriz se colocarán en las ubicaciones correspondientes del rectángulo.
  
Si usa una matriz horizontal para el segundo argumento, se duplica hacia abajo para rellenar todo el rectángulo. Si usa una matriz vertical, se duplica a la derecha para rellenar todo el rectángulo. Si usa una matriz rectangular y es demasiado pequeña para el intervalo rectangular en el que desea colocarla, dicho intervalo se agrega con **#N/A.**
  
Si el rango de destino es menor que la matriz de origen, los valores se copian hasta los límites del rango de destino y se omiten los datos adicionales.
  
Para borrar un elemento del rectángulo de destino, use un elemento de matriz de tipo **xltypeNil** en la matriz de origen. Para borrar todo el rectángulo de destino, omita el segundo argumento. 
  
### <a name="restrictions"></a>Restricciones

**xlSet** no se puede deshacer. Además, destruye cualquier información de deshacer que haya estado disponible antes. 
  
**xlSet** sólo puede colocar constantes, no fórmulas, en celdas. 
  
**xlSet se** comporta como una función equivalente a un comando de clase 3; es decir, solo está disponible dentro de una DLL cuando se llama a la DLL  desde un objeto, macro,  menú, barra de herramientas, tecla de método  abreviado o el botón Ejecutar en el cuadro de diálogo **Macro** (al que se tiene acceso desde la pestaña Ver de la cinta de opciones a partir de Excel 2007 y el menú Herramientas en versiones anteriores). 
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo se rellena B205:B206 con el valor que se pasó desde una macro. Este ejemplo de función de comando requiere un argumento, por lo que solo funcionará si se llama desde una hoja de macros XLM o desde un módulo VBA mediante el **método Application.Run.** 
  
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

## <a name="see-also"></a>Consulte también

- [xlCoerce](xlcoerce.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

