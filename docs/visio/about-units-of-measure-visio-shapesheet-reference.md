---
title: Acerca de las unidades de medida (referencia de ShapeSheet de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251828
localization_priority: Normal
ms.assetid: 48f765a8-7485-03c0-3484-d4ec07822600
description: Al insertar campos en texto o crear fórmulas, a menudo especificará unidades de medida para los valores.
ms.openlocfilehash: ce8ad1cdcbdaba713edeb06f4cd949e49f82a311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821510"
---
# <a name="about-units-of-measure-visio-shapesheet-reference"></a>Acerca de las unidades de medida (referencia de ShapeSheet de Visio)

Al insertar campos en texto o crear fórmulas, a menudo especificará unidades de medida para los valores.
  
Microsoft Visio evalúa el resultado de una fórmula de forma diferente dependiendo de la celda en la que se escriba la fórmula. En general, las celdas que representan la posición de la forma, una dimensión o un ángulo requieren una pareja número y unidad que consta de un número y las unidades necesarias para interpretar el número. Muchas otras celdas no requieren unidades y evaluar en una cadena, TRUE o FALSE o a un índice. Por ejemplo, la misma fórmula que en la celda **FillForegnd** significa el color 5 de la paleta de colores del dibujo significa TRUE (y bloquea el ancho de la forma) en la celda LockWidth. 
  
Especifique siempre la unidad de medida cuando escriba una fórmula en una celda que requiera un valor dimensional. Si no especifica una unidad de medida, Visio utilizará la predeterminada para la celda, que puede ser unidades de página, de dibujo, de duración o de ángulo.
  
## <a name="units-of-measure"></a>Unidades de medida

Cuando quiera indicar unidades de medida en las fórmulas de ShapeSheet, utilice las abreviaturas que aparecen en la tabla siguiente.
  
|**Para especificar estas unidades de medida**|**Uso**|**Constante de automatización**|
|:-----|:-----|:-----|
| Centímetros  <br/> | cm  <br/> |**visCentimeters (69)** <br/> |
| Cíceros  <br/> | c  <br/> |**visCiceros (54)** <br/> |
| Fecha u hora  <br/> | fecha  <br/> |**visDate (40)** <br/> |
| Grados  <br/> | grad  <br/> |**visDegrees (81)** <br/> |
| Didots  <br/> | d  <br/> |**visDidots (53)** <br/> |
| Semanas transcurridas  <br/> | st  <br/> |**visElapsedWeek (43)** <br/> |
| Días transcurridos  <br/> | dt  <br/> |**visElapsedDay (44)** <br/> |
| Horas transcurridas  <br/> | ht  <br/> |**visElapsedHour (45)** <br/> |
| Minutos transcurridos  <br/> | mt  <br/> |**visElapsedMin (46)** <br/> |
| Segundos transcurridos  <br/> | es  <br/> |**visElapsedSec (47)** <br/> |
| Pies  <br/> | ft  <br/> |**visFeet (66)** <br/> |
| Pulgadas  <br/> | in  <br/> |**visInches (65)** <br/> |
| Kilómetros  <br/> | km  <br/> |**visKilometers (72)** <br/> |
| Metros  <br/> | m  <br/> |**visMeters (71)** <br/> |
| Millas  <br/> | mi  <br/> |**visMiles (68)** <br/> |
| Milímetros  <br/> | mm  <br/> |**visMillimeters (70)** <br/> |
| Minutos  <br/> | '  <br/> |**visMin (84)** <br/> |
| Millas náuticas  <br/> | nm  <br/> |**visNautMiles (76)** <br/> |
| Porcentaje  <br/> | %  <br/> |**visPercent (33)** <br/> |
| Picas  <br/> | p  <br/> |**visPicas (51)** <br/> |
| Puntos  <br/> | pt  <br/> |**visPoints (50)** <br/> |
| Radianes  <br/> | rad  <br/> |**visRadians (83)** <br/> |
| Segundos  <br/> | "  <br/> |**visSec (85)** <br/> |
| Yardas  <br/> | yd  <br/> |**visYards (75)** <br/> |
   
## <a name="compound-units-of-measure"></a>Unidades compuestas de medida

En las fórmulas, puede expresar las unidades de medida de los números compuestos con las abreviaturas en la siguiente tabla. Visio simplifica los resultados y los muestra en las unidades compuestas.
  
Por ejemplo, si escribe 45,635º, Visio mostrará el valor equivalente 45° 38' 6".
  
|**Para especificar las unidades**|**Use esta abreviatura**|**Constante de automatización**|
|:-----|:-----|:-----|
| Cíceros y didots  <br/> | CICERO/DIDOT  <br/> |**visCicerosAndDidots (52)** <br/> |
| Grados, minutos y segundos  <br/> | °  <br/> |**visDegreeMinSec (82)** <br/> |
| Pies y pulgadas  <br/> | FEET/INCH  <br/> |**visFeetAndInches (67)** <br/> |
| Picas y puntos  <br/> | PICAPOINTS  <br/> |**visPicasAndPoints (49)** <br/> |
   
## <a name="fractional-units-of-measure"></a>Unidades de medida fraccionarias

Puede especificar unidades de medida fraccionarias en la celda **DrawingScale** para afectar al número de subdivisiones de regla que Visio muestra en la ventana de dibujo. De forma predeterminada, Visio divide las distancias en diez subdivisiones al mostrar las reglas. Si utiliza unidades de medida fraccionarias en la celda **DrawingScale** , Visio dividirá la distancia en lo siguiente: 
  
- Octavos para *visInchFrac* y *visMileFrac* 
    
- Doceavos para *visFeetAndInches* 
    
Las unidades de medida fraccionarias no tienen ningún efecto en las celdas distintas de DrawingScale.
  
|**Para especificar unidades fraccionarias**|**Use esta abreviatura**|**Constante de automatización**|
|:-----|:-----|:-----|
| Pulgadas en fracciones  <br/> | IN_F  <br/> |**visInchFrac (73)** <br/> |
| Millas en fracciones  <br/> | MI_F  <br/> |**visMileFrac (74)** <br/> |
| Pies y pulgadas  <br/> | FEET/INCH  <br/> |**visFeetAndInches (67)** <br/> |
   
## <a name="multidimensional-units-of-measure"></a>Unidades multidimensionales de medida

En las fórmulas, puede expresar las unidades de medida de los números multidimensionales con las abreviaturas de la tabla siguiente. Visio simplifica los resultados y los muestra con las unidades multidimensionales.
  
|**Para especificar unidades multidimensionales**|**Use esta abreviatura**|**Constante de automatización**|
|:-----|:-----|:-----|
| Acre  <br/> | ACRES  <br/> |**visAcre (36)** <br/> |
| Centímetros  <br/> | CM CUADRADOS, CM. CUADRADOS, CM.^2, CM^2  <br/> |**visCentimeters (69)** <br/> |
| Pies  <br/> | PIES CUADRADOS, PIES^2  <br/> |**visFeet (66)** <br/> |
| Hectáreas  <br/> | HECTÁREAS, HECTÁREA, HA., HA  <br/> |**visHectare (37)** <br/> |
| Pulgadas  <br/> | PDA. CUADRADAS, PDA CUADRADAS, PDA.^2, PDA^2  <br/> |**visInches (65)** <br/> |
| Kilómetros  <br/> | KM. CUADRADOS, KM CUADRADOS, KM.^2, KM ^2  <br/> |**visKilometers (72)** <br/> |
| Metros  <br/> | M. CUADRADOS, M CUADRADOS, M.^2, M ^2  <br/> |**visMeters (71)** <br/> |
| Millas  <br/> | MI. CUADRADAS, MI CUADRADAS, MI.^2, MI ^2  <br/> |**visMiles (68)** <br/> |
| Milímetros  <br/> | MM. CUADRADOS, MM CUADRADOS, MM.^2, MM ^2  <br/> |**visMillimeters (70)** <br/> |
| Yardas  <br/> | YD. CUADRADAS, YD CUADRADAS, YD.^2, YD^2  <br/> |**visYards (75)** <br/> |
   
## <a name="universal-strings"></a>Cadenas universales

En las versiones traducidas de Visio, el conjunto de cadenas reconocidas cambia para cada idioma. Si desea que un programa funcione en varios idiomas, utilice las cadenas universales para las unidades de medida.
  
|**Para**|**Use**|
|:-----|:-----|
| Centímetros  <br/> | CM  <br/> |
| Cíceros  <br/> | C  <br/> |
| Cíceros y didots  <br/> | CICERO/DIDOT  <br/> |
| Fecha u hora  <br/> | DATE  <br/> |
| Grados  <br/> | DEG  <br/> |
| Grados, minutos, segundos  <br/> | °  <br/> |
| Didots  <br/> | D  <br/> |
| Semanas transcurridas  <br/> | EW  <br/> |
| Días transcurridos  <br/> | ED  <br/> |
| Horas transcurridas  <br/> | EH  <br/> |
| Minutos transcurridos  <br/> | EM  <br/> |
| Segundos transcurridos  <br/> | ES  <br/> |
| Pies  <br/> | FT  <br/> |
| Pies y pulgadas  <br/> | FEET/INCH  <br/> |
| Pulgadas  <br/> | IN  <br/> |
| Pulgadas en fracciones  <br/> | IN_F  <br/> |
| Kilómetros  <br/> | KM  <br/> |
| Metros  <br/> | M  <br/> |
| Millas  <br/> | MI  <br/> |
| Millas en fracciones  <br/> | MI_F  <br/> |
| Milímetros  <br/> | MM  <br/> |
| Minutos  <br/> | '  <br/> |
| Millas náuticas  <br/> | NM  <br/> |
| Porcentaje  <br/> | %  <br/> |
| Picas  <br/> | P  <br/> |
| Picas y puntos  <br/> | PICAPOINTS  <br/> |
| Puntos  <br/> | PT  <br/> |
| Radianes  <br/> | RAD  <br/> |
| Segundos  <br/> | "  <br/> |
| Yardas  <br/> | YD  <br/> |
   
## <a name="implicit-units-of-measure"></a>Unidades implícitas de medida

Cuando Visio analiza y almacena una pareja número y unidad, puede utilizar unidades implícitas o explícitas. Un número expresado en unidades explícitas siempre aparecerá en las unidades de medida especificadas originalmente. Un número expresado en unidades implícitas siempre se convertirá al valor equivalente en las unidades de dibujo, página o ángulo adecuadas para la celda.
  
Por ejemplo, supongamos que especifica el equivalente de 1 pulgada en la celda A con unidades explícitas y en la celda B con unidades implícitas, y que tanto A como B utilizan unidades de dibujo. A continuación, cambia las unidades predeterminadas de la página a centímetros. En la celda A seguirá apareciendo 1 pda., porque utiliza unidades explícitas que no cambian cuando cambian los valores predeterminados. En la celda B aparece ahora 2,54 cm, el valor equivalente en las unidades predeterminadas.
  
Para especificar unidades implícitas, utilice la sintaxis siguiente:
  
```vb
number  [unit , flag ]
```

|||
|:-----|:-----|
| _number_ <br/> |Valor original, como 3,7, 1,7E-4 ó 5 1/2.  <br/> |
| _unit_ <br/> |Unidades en que se expresa originalmente el _número_ .  <br/> |
| _flag_ <br/> |Sistema de medida que se utiliza cuando se muestra la unidad implícita. Vea los valores a continuación.  <br/> |
   
El parámetro _marca_ es una de las letras siguientes (mayúsculas o minúsculas) e indica el sistema de medida que se debe usar cuando se muestra el valor en unidades implícitas. 
  
|**_Flag_**|**Sistema de medida**|**Ejemplo**|
|:-----|:-----|:-----|
| a, A  <br/> | Angular  <br/> | =5[deg,A]  <br/> |
| d, D  <br/> | Dibujo  <br/> | =5[in,D]  <br/> |
| e, E  <br/> | Duración  <br/> | =5[eh,E]  <br/> |
| p, P  <br/> | Page  <br/> | =5[in,P]  <br/> |
| t, T  <br/> | Tipo  <br/> | =5[pt,T]  <br/> |
   
Además, puede utilizar las unidades implícitas DL, DP, DT, DA, DE para implícitas dibujo, página, texto-, angular-y unidades de tiempo, respectivamente. Estas unidades se suponen que el valor asociado es unidades internas. Por ejemplo, si el sistema de medida actual es centímetros, *= 2 DL* sería se interpretará como 2 unidades internas (pulgadas) y mostrará como 5,08 cm. 
  
Con la sintaxis implícita descrita anteriormente, esta expresión (=2 DL) equivale a 2[pda,d]. La sintaxis implícita le permite elegir cómo se interpretará el valor, de modo que también podría especificar 2[pies,d], que se interpretaría como 2 pies y se mostraría como 60,96 cm. Las unidades implícitas DL, DP, DT, DA y DE son universales y no tienen una traducción equivalente.
  
## <a name="default-units-of-measure"></a>Unidades de medida predeterminadas

A continuación se enumeran las unidades de medida predeterminadas, junto con la configuración equivalente en la interfaz de usuario.
  
|**Unidad de medida predeterminada**|**Equivalente en la interfaz de usuario**|
|:-----|:-----|
|**visDrawingUnits** <br/> |Unidades de la celda DrawingScale de la página o patrón que contiene la celda.  <br/> |
|**visPageUnits** <br/> |Unidades seleccionadas en el cuadro **Unidades de medida** de la ficha **Propiedades de página** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha **Configurar página**). 
  <br/> |
|**visTypeUnits** <br/> |Unidades seleccionadas en el cuadro de **texto** bajo **Mostrar** en la ficha **Avanzadas** del cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** y, a continuación, haga clic en **Opciones**).  <br/> |
|**visAngleUnits** <br/> |Unidades seleccionadas en el cuadro **Ángulo** en **Presentación**, en la ficha **Opciones avanzadas** del cuadro de diálogo **Opciones de Visio**.  <br/> |
|**visDurationUnits** <br/> |Unidades seleccionadas en el cuadro **Duración** en **Presentación**, en la ficha **Opciones avanzadas** del cuadro de diálogo **Opciones de Visio**.  <br/> |
   

