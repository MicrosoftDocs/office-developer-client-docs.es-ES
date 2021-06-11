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
description: 'Las fórmulas pueden contener cadenas. Para dar formato a la presentación de una cadena, por ejemplo, en una celda que pide datos, el valor de un elemento de datos de formas o un campo de texto, se especifica una imagen de formato. El resultado puede tener formato de par número-unidad, cadena, fecha-hora, duración o moneda. Por ejemplo, el formato picture0 #/10 uuformats the number-unit pair 10.9cm as10 9/10 centimeters.'
ms.openlocfilehash: aa95e11db387913edbb40292f7da6a0f4b8a5cf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409520"
---
# <a name="about-strings"></a>Cadenas

Las fórmulas pueden contener cadenas. Para dar formato a la presentación de una cadena, por ejemplo, en una celda que pide datos, el valor de un elemento de datos de formas o un campo de texto, se especifica una imagen de formato. El resultado puede tener formato de par número-unidad, cadena, fecha-hora, duración o moneda. Por ejemplo, la imagen de formato "0 #/10 uu" muestra el par número-unidad 10,9 cm como "10 9/10 centímetros".
  
Puede usar el formato de imágenes en la celda **Formato** de la sección Datos de formas y como argumento para la **función FORMAT** o **FORMATEX.** Al insertar un campo de texto, las imágenes de formato aparecen en la lista de formatos del cuadro de diálogo **Campo** (ficha **Insertar**). 
  
## <a name="using-functions-to-format-strings"></a>Uso de funciones para dar formato a las cadenas

En cualquier fórmula que se resuelva en una cadena, incluidas las fórmulas de campo de texto personalizadas, puede usar la **función FORMAT** o **FORMATEX.** La función FORMAT devuelve una cadena que contiene la salida con formato. La **función FORMATEX** convierte la entrada sin escribir en las unidades que elija para el resultado con formato. 
  
## <a name="displaying-formatted-shape-data"></a>Presentación de datos de formas con formato

Para dar formato al valor mostrado de un elemento de datos de formas puede especificar una imagen de formato en la celda Format.
  
Por ejemplo, una forma línea de tiempo de un proyecto puede tener una propiedad personalizada que mida el costo de un proceso. De forma predeterminada, el valor de un elemento de datos de formas es una cadena. Para dar formato a la cadena "1200", puede especificar "###.###,00 $" en la celda Format para que el usuario vea un valor de moneda.
  
Microsoft Visio usa las configuraciones de la ficha **Moneda** del cuadro de diálogo **Personalizar formato** del elemento de **configuración regional y de idioma** del Panel de control para determinar el símbolo de moneda y el separador de miles que debe mostrar. (En **el Panel de control,** haga clic en Región e **idioma** y, a continuación, haga clic **en Configuración**.)
  
Para convertir una cadena en un valor de moneda que pueda utilizar posteriormente en cálculos, utilice la función CY.
  
## <a name="using-functions-to-manipulate-text-strings"></a>Uso de funciones para manipular las cadenas de texto

Puede utilizar funciones para manipular las cadenas de texto, por ejemplo, para localizar o sustituir determinados caracteres en una cadena. También puede obtener información acerca de la posición de un carácter en una cadena o identificar los caracteres iniciales y finales en una cadena de texto. 
  

