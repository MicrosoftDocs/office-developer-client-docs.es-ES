---
title: Referencias hoja de cálculo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- references [excel 2007], worksheet,worksheet references [Excel 2007],external worksheet references [Excel 2007],active worksheet [Excel 2007],current worksheet [Excel 2007],internal worksheet references [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2944f73a3144837a4be8aff7c7fed9a8d2158203
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416464"
---
# <a name="worksheet-references"></a>Referencias de hojas de cálculo

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Una referencia en Microsoft Excel es un tipo de datos que hace referencia a un bloque rectangular de celdas (que pueden ser una sola celda) o, en algunos casos, un número de bloques de celdas no contiguas. Internamente, Excel usa un tipo de referencia para las celdas de la hoja actual, conocido como una referencia interna. Cualquier celda que no se encuentre en la hoja actual se describe con otro tipo de referencia conocida como referencia externa. Consulte la siguiente sección para obtener la definición del activo y el actual.
  
## <a name="active-vs-current"></a>Activo y actual

En Excel, el término activo hace referencia a lo que el usuario ve. La hoja de cálculo y el libro activos son los que el usuario está viendo o, si Excel ha perdido el foco en otra aplicación, lo que estaban viendo cuando Excel tenía el último foco. La hoja activa se encuentra siempre en el libro activo. La celda o celdas seleccionadas en la hoja activa se conocen como celdas activas. Si un objeto integrado tiene el foco, las últimas celdas seleccionadas seguirán siendo activas. 
  
El término actual hace referencia a lo que Excel recalcula. El libro y la hoja de cálculo actuales son los que actualmente se recalculan. La hoja actual siempre se encuentra en el libro actual. La celda que se recalcula se conoce como la celda actual o, en el caso de una fórmula de matriz que se recalcula, las celdas actuales. 
  
Los puntos importantes a recordar son los siguientes:
  
- Normalmente, el libro, la hoja de cálculo o la celda activos no son los actuales, aunque pueden serlo.
    
- Una función de complemento, ya sea en un módulo de Visual Basic para aplicaciones (VBA), o un DLL o XLL, siempre se llama desde la celda actual en la hoja actual, o uno de ellos en el caso de la actualización multiproceso (MTR).
    
Muchas funciones de Excel que proporcionan información sobre una celda, un rango de celdas o una hoja de un libro, distinguen entre el libro, la hoja o la celda activos, y el libro, la hoja o la celda actuales. Esta diferencia se refleja en los tipos de datos que se usan para describir las referencias a bloques de celdas, como se describe en la siguiente sección.
  
## <a name="internal-and-external-worksheet-references"></a>Referencias de hoja de cálculo internas y externas

La diferencia principal entre las referencias internas y externas es que el tipo de datos de referencia externa contiene un identificador para la hoja de cálculo y también una descripción de las celdas a las que hace referencia. Una referencia interna no contiene ninguna referencia a la hoja, es implícito que la hoja es la hoja actual. 
  
Muchas funciones de la API de C devuelven referencias o toman argumentos de referencia. Cualquier función de la API de C que toma argumentos de referencia acepta referencias externas o internas, excepto la función **xlSheetNm**, que necesita una referencia externa. Algunas funciones solo devuelven referencias internas o externas. Por ejemplo, la función de la API de C [xlfCaller](xlfcaller.md) devuelve una referencia a las celdas de la llamada, por definición, en la hoja actual. La referencia devuelta es siempre una referencia interna, aunque la función puede devolver tipos de no referencia donde no se llama a la función desde una celda de la hoja de cálculo. La función de la API de C [xlSheetId ](xlsheetid.md) siempre devuelve el identificador de una hoja de cálculo dentro de un tipo de datos de referencia externa. 
  
La otra diferencia clave entre los tipos de referencia internos y externos es que el tipo de datos de referencia externa puede describir bloques de celdas no contiguos en la misma hoja. Las referencias internas solo pueden describir un único bloque en la hoja actual. Las referencias no contiguas se pueden pasar a cualquier función que tome un argumento de rango.
  
## <a name="see-also"></a>Vea también



[Conceptos de programación de Excel](excel-programming-concepts.md)
  
[Evaluar los nombres y otras expresiones de fórmulas de la hoja de cálculo](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Evaluación de expresiones y hojas de cálculo de Excel](excel-worksheet-and-expression-evaluation.md)

