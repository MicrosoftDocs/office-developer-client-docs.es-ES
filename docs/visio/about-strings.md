---
title: Cadenas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251826
localization_priority: Normal
ms.assetid: e1174d8f-70cb-4595-7906-889da15367db
description: 'Las fórmulas pueden contener cadenas. Para aplicar el formato de salida de cadena, como en una celda prompt, un valor de elemento de datos de formas o un campo de texto, especifique un formato de imagen. Puede tener un formato de salida como un par de número de unidad, cadena, fecha y hora, duración o moneda. Por ejemplo, el uuformats de #/ 10 de formato picture0 la unidad de número par 10,9 cm as10 9/10 centímetros.'
ms.openlocfilehash: 1fd003ecd5c824042e97a40fa8374aeead254ddc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821489"
---
# <a name="about-strings"></a>Información sobre cadenas

Las fórmulas pueden contener cadenas. Para dar formato a la presentación de una cadena, por ejemplo, en una celda que pide datos, el valor de un elemento de datos de formas o un campo de texto, se especifica una imagen de formato. El resultado puede tener formato de par número-unidad, cadena, fecha-hora, duración o moneda. Por ejemplo, la imagen de formato "0 #/10 uu" muestra el par número-unidad 10,9 cm como "10 9/10 centímetros".
  
Puede utilizar imágenes de formato en la celda **Format** de la sección datos de formas y como un argumento a la función **FORMAT** o **FORMATEX** . Cuando se inserta un campo de texto, imágenes de formato aparecen en la lista de formatos en el cuadro de diálogo **campo** (ficha**Insertar** ). 
  
## <a name="using-functions-to-format-strings"></a>Uso de funciones para dar formato a las cadenas

Puede usar la función **FORMAT** o **FORMATEX** en cualquier fórmula que se resuelve en una cadena, incluidas las fórmulas de campo de texto personalizado. La función FORMAT devuelve una cadena de la salida con formato. La función **FORMATEX** convierte un argumento de entrada a las unidades que elija para el resultado con formato. 
  
## <a name="displaying-formatted-shape-data"></a>Presentación de datos de formas con formato

Para dar formato al valor mostrado de un elemento de datos de formas puede especificar una imagen de formato en la celda Format.
  
Por ejemplo, una forma línea de tiempo de un proyecto puede tener una propiedad personalizada que mida el costo de un proceso. De forma predeterminada, el valor de un elemento de datos de formas es una cadena. Para dar formato a la cadena "1200", puede especificar "###.###,00 $" en la celda Format para que el usuario vea un valor de moneda.
  
Microsoft Visio usa la configuración en la ficha **moneda** en el cuadro de diálogo **Personalizar el formato** en el elemento **regional e idioma** en el Panel de Control para determinar el símbolo de moneda y miles separador que se debe mostrar. (En el **Panel de Control**, haga clic en **idioma y región**y, a continuación, haga clic en **Configuración adicional**).
  
Para convertir una cadena en un valor de moneda que pueda utilizar posteriormente en cálculos, utilice la función CY.
  
## <a name="using-functions-to-manipulate-text-strings"></a>Uso de funciones para manipular las cadenas de texto

Puede utilizar funciones para manipular las cadenas de texto, por ejemplo, para localizar o sustituir determinados caracteres en una cadena. También puede obtener información acerca de la posición de un carácter en una cadena o identificar los caracteres iniciales y finales en una cadena de texto. 
  

