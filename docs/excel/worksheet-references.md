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
ms.openlocfilehash: b7089fb891c96be9182189e3a5f30057721cebbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815720"
---
# <a name="worksheet-references"></a>Referencias de hojas de cálculo

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Una referencia en Microsoft Excel es un tipo de datos que hace referencia a un bloque rectangular de celdas (que pueden ser una sola celda) o, en algunos casos, un n�mero de bloques de celdas no contiguas. Internamente, Excel usa un tipo de referencia para las celdas de la hoja actual, conocido como una referencia interna. Cualquier celda que no se encuentre en la hoja actual se describe con otro tipo de referencia conocida como referencia externa. Consulte la siguiente secci�n para obtener la definici�n del activo y el actual.
  
## <a name="active-vs-current"></a>Activo y actual

En Excel, el t�rmino activo hace referencia a lo que el usuario ve. La hoja de cálculo y el libro activos son los que el usuario est� viendo o, si Excel ha perdido el foco en otra aplicación, lo que estaban viendo cuando Excel ten�a el �ltimo foco. La hoja activa se encuentra siempre en el libro activo. La celda o celdas seleccionadas en la hoja activa se conocen como celdas activas. Si un objeto integrado tiene el foco, las �ltimas celdas seleccionadas seguir�n siendo activas. 
  
El t�rmino actual hace referencia a lo que Excel recalcula. El libro y la hoja de cálculo actuales son los que actualmente se recalculan. La hoja actual siempre se encuentra en el libro actual. La celda que se recalcula se conoce como la celda actual o, en el caso de una fórmula de matriz que se recalcula, las celdas actuales. 
  
Los puntos importantes a recordar son los siguientes:
  
- Normalmente, el libro, la hoja de cálculo o la celda activos no son los actuales, aunque pueden serlo.
    
- Una función de complemento, ya sea en un m�dulo de Visual Basic para aplicaciones (VBA), o un DLL o XLL, siempre se llama desde la celda actual en la hoja actual, o uno de ellos en el caso de la actualizaci�n multiproceso (MTR).
    
Muchas funciones de Excel que proporcionan información sobre una celda, un rango de celdas o una hoja de un libro, distinguen entre el libro, la hoja o la celda activos, y el libro, la hoja o la celda actuales. Esta diferencia se refleja en los tipos de datos que se usan para describir las referencias a bloques de celdas, como se describe en la siguiente secci�n.
  
## <a name="internal-and-external-worksheet-references"></a>Referencias de hoja de cálculo internas y externas

La diferencia principal entre las referencias internas y externas es que el tipo de datos de referencia externa contiene un identificador para la hoja de cálculo y tambi�n una descripci�n de las celdas a las que hace referencia. Una referencia interna no contiene ninguna referencia a la hoja, es impl�cito que la hoja es la hoja actual. 
  
Muchas funciones de la API de C devuelven referencias o toman argumentos de referencia. Cualquier función de la API de C que toma argumentos de referencia acepta referencias externas o internas, excepto la función **xlSheetNm**, que necesita una referencia externa. Algunas funciones solo devuelven referencias internas o externas. Por ejemplo, la función de la API de C [xlfCaller](xlfcaller.md) devuelve una referencia a las celdas de la llamada, por definici�n, en la hoja actual. La referencia devuelta es siempre una referencia interna, aunque la función puede devolver tipos de no referencia donde no se llama a la función desde una celda de la hoja de cálculo. La función de la API de C [xlSheetId ](xlsheetid.md) siempre devuelve el identificador de una hoja de cálculo dentro de un tipo de datos de referencia externa. 
  
La otra diferencia clave entre los tipos de referencia internos y externos es que el tipo de datos de referencia externa puede describir bloques de celdas no contiguos en la misma hoja. Las referencias internas solo pueden describir un �nico bloque en la hoja actual. Las referencias no contiguas se pueden pasar a cualquier función que tome un argumento de rango.
  
## <a name="see-also"></a>Vea también



[Conceptos de programación de Excel](excel-programming-concepts.md)
  
[Evaluaci�n de nombres y otras expresiones de fórmula de la hoja de cálculo](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Hojas de cálculo y evaluaci�n de expresiones de Excel](excel-worksheet-and-expression-evaluation.md)

