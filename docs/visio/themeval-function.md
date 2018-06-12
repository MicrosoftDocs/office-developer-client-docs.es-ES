---
title: THEMEVAL (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: Recupera los valores de tema activo.
ms.openlocfilehash: 7bbd017c859a0a167bbd279d60af029e98421375
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823408"
---
# <a name="themeval-function"></a>THEMEVAL (función)

Recupera los valores de tema activo. 
  
## <a name="version-information"></a>Información de versión

Versión agregada: Visio 2013 
  
## <a name="syntax"></a>Sintaxis

 **THEMEVAL** ([ _"theme_value"_] [, _predeterminado_]) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _"theme_value"_ <br/> |Opcional  <br/> |**String** <br/> |El nombre de una celda en la definición de tema para obtener un valor desde.  <br/> |
| _default_ <br/> |Opcional  <br/> |Varios  <br/> |Un valor predeterminado si el documento no es con temas (no hay ninguna definición de tema).  <br/> |
   
## <a name="remarks"></a>Notas

Si la función **THEMEVAL** no recibe ningún argumento, devuelve el valor de la celda de host con temas. Esto es el valor almacenado en la definición del tema actual. La celda de host debe ser capaz de ser con temas para devolver un valor; Si la celda no es capaz de ser con temas, **THEMEVAL** devuelve un error. 
  
Si la función **THEMEVAL** recibe un único argumento, se recupera el valor de la definición del tema que se pasó como argumento. El argumento que se pasa en para el primer parámetro debe ser un número entero o una de las cadenas exactas que aparecen en la tabla siguiente. 
  
La función **THEMEVAL** también puede aceptar un número entero para el primer parámetro, como un valor entre 1 y 8. Uso de valores enteros, recupera un color por índice a partir de la combinación de colores del tema. Por lo tanto, un valor de '1' devolverá el color "Oscuro" del tema, '2' devuelve el color de "Claro", '3' devuelve el color de "Énfasis 1", etcetera. 
  
Si la función **THEMEVAL** recibe dos argumentos, se recupera el valor de la definición del tema que se pasó como primer argumento. Sin embargo, si el documento tiene sin tema que se ha aplicado, a continuación, la función **THEMEVAL** usa el valor especificado como segundo argumento. 
  
**Posibles argumentos para el parámetro "theme_value"**

|**Valor**|**Descripción**|
|:-----|:-----|
|"Oscuro"  <br/> |Recupera la definición de tema color RGB oscuro.  <br/> |
|"Claro"  <br/> |Recupera el color RGB claro de la definición de tema.  <br/> |
|"BackgroundColor"  <br/> |Recupera el color de fondo RGB de la definición del tema.  <br/> |
|"AccentColor"  <br/> |Recupera el color de énfasis 1 RGB de la definición del tema.  <br/> |
|"AccentColor2"  <br/> |Recupera el color de énfasis 2 RGB de la definición del tema.  <br/> |
|"AccentColor3"  <br/> |Recupera el color de énfasis 3 RGB de la definición del tema.  <br/> |
|"AccentColor4"  <br/> |Recupera el color de énfasis 4 RGB de la definición del tema.  <br/> |
|"AccentColor5"  <br/> |Recupera el color de énfasis 5 RGB de la definición del tema.  <br/> |
|"AccentColor6"  <br/> |Recupera el color RGB Accent6 de la definición del tema.  <br/> |
|"LinePattern"  <br/> |Recupera el valor de la celda LinePattern de la definición del tema.  <br/> |
|"LineWeight"  <br/> |Recupera el valor de la celda LineWeight de la definición del tema.  <br/> |
|"LineColor"  <br/> |Recupera el valor de la celda LineColor de la definición del tema.  <br/> |
|"LineCap"  <br/> |Recupera el valor de la celda LineCap de la definición del tema.  <br/> |
|"LineBegin"  <br/> |Recupera el valor de la celda BeginArrow de la definición del tema.  <br/> |
|"LineEnd"  <br/> |Recupera el valor de la celda EndArrow de la definición del tema.  <br/> |
|"LineColorTrans"  <br/> |Recupera el valor de la celda LineColorTrans de la definición del tema.  <br/> |
|"LineCompoundtype"  <br/> |Recupera el valor de la celda CompoundType desde la definición de tema.  <br/> |
|"LineBegin"  <br/> |Recupera el valor de la celda BeginArrow de la definición del tema.  <br/> |
|"LineEnd"  <br/> |Recupera el valor de la celda EndArrow de la definición del tema.  <br/> |
|"LineBeginSize"  <br/> |Recupera el valor de la celda BeginArrowSize de la definición del tema.  <br/> |
|"LineEndSize"  <br/> |Recupera el valor de la celda EndArrowSize de la definición del tema.  <br/> |
|"LineRounding"  <br/> |Recupera el valor de la celda Rounding de la definición del tema.  <br/> |
|"ConnectorColor"  <br/> |Recupera el valor de la celda LineColor de la definición del tema.  <br/> |
|"ConnectorPattern"  <br/> |Recupera el valor de la celda LinePattern de la definición del tema.  <br/> |
|"ConnectorWeight"  <br/> |Recupera el valor de la celda LineWeight de la definición del tema.  <br/> |
|"ConnectorTransparency"  <br/> |Recupera el valor de la celda LineColorTrans de la definición del tema.  <br/> |
|"ConnectorRounding"  <br/> |Recupera el valor de la celda Rounding de la definición del tema.  <br/> |
|"ConnectorBegin"  <br/> |Recupera el valor de la celda BeginArrow de la definición del tema.  <br/> |
|"Connectorenddebe"  <br/> |Recupera el valor de la celda EndArrow de la definición del tema.  <br/> |
|"ConnectorBeginSize"  <br/> |Recupera el valor de la celda BeginArrowSize de la definición del tema.  <br/> |
|"ConnectorEndSize"  <br/> |Recupera el valor de la celda EndArrowSize de la definición del tema.  <br/> |
|"FillColor"  <br/> |Recupera el valor de la celda FillForegnd de la definición del tema.  <br/> |
|"FillColor2"  <br/> |Recupera el valor de la celda FillBkgnd de la definición del tema.  <br/> |
|"FillTransparency"  <br/> |Recupera el valor de la celda FillForegndTrans de la definición del tema.  <br/> |
|"FillPattern"  <br/> |Recupera el valor de la celda FillPattern de la definición del tema.  <br/> |
|"LineGradientEnabled"  <br/> |Recupera el valor de la celda LineGradientEnabled desde la definición de tema.  <br/> |
|"LineGradientDir"  <br/> |Recupera el valor de la celda LineGradientDir desde la definición de tema.  <br/> |
|"LineGradientAngle"  <br/> |Recupera el valor de la celda LineGradientAngle desde la definición de tema.  <br/> |
|"FillGradientEnabled"  <br/> |Recupera el valor de la celda FillGradientEnabled desde la definición de tema.  <br/> |
|"FillGradientDir"  <br/> |Recupera el valor de la celda FillGradientDir desde la definición de tema.  <br/> |
|"FillGradientAngle"  <br/> |Recupera el valor de la celda FillGradientAngle desde la definición de tema.  <br/> |
|"RotateGradientWithShape"  <br/> |Recupera el valor de la celda RotateGradientWithShape desde la definición de tema.  <br/> |
|"UseGroupGradient"  <br/> |Recupera el valor de la celda UseGroupGradient desde la definición de tema.  <br/> |
|"ShadowType"  <br/> |Recupera el valor de la celda ShapeShdwType de la definición del tema.  <br/> |
|"ShadowColor"  <br/> |Recupera el valor de la celda ShdwColor desde la definición de tema.  <br/> |
|"ShadowTransparency"  <br/> |Recupera el valor de la celda ShdwColorTrans desde la definición de tema.  <br/> |
|"ShadowMagnification"  <br/> |Recupera el valor de la celda ShapeShdwScaleFactor de la definición del tema.  <br/> |
|"ShadowBlur"  <br/> |Recupera el valor de la celda ShapeShdwBlur desde la definición de tema.  <br/> |
|"ShadowXOffset"  <br/> |Recupera el valor de la celda ShapeShdwOffsetX de la definición del tema.  <br/> |
|"ShadowYOffset"  <br/> |Recupera el valor de la celda ShapeShdwOffsetY de la definición del tema.  <br/> |
|"ShadowDirection"  <br/> |Recupera el valor de la celda ShapeShdwObliqueAngle de la definición del tema.  <br/> |
|"ShadowPattern"  <br/> |Recupera el valor de la celda ShdwPattern de la definición del tema.  <br/> |
|"BevelTopType"  <br/> |Recupera el valor de la celda BevelTopType desde la definición de tema.  <br/> |
|"BevelTopWidth"  <br/> |Recupera el valor de la celda BevelTopWidth desde la definición de tema.  <br/> |
|"BevelTopHeight"  <br/> |Recupera el valor de la celda BevelTopHeight desde la definición de tema.  <br/> |
|"BevelMaterial"  <br/> |Recupera el valor de la celda BevelMaterialType desde la definición de tema.  <br/> |
|"BevelLighting"  <br/> |Recupera el valor de la celda BevelLightingType desde la definición de tema.  <br/> |
|"BevelLightingAngle"  <br/> |Recupera el valor de la celda BevelLightingAngle desde la definición de tema.  <br/> |
|"BevelContourColor"  <br/> |Recupera el valor de la celda BevelContourColor desde la definición de tema.  <br/> |
|"BevelContourSize"  <br/> |Recupera el valor de la celda BevelContourSize desde la definición de tema.  <br/> |
|"ReflectionBlur"  <br/> |Recupera el valor de la celda ReflectionBlur desde la definición de tema.  <br/> |
|"ReflectionDist"  <br/> |Recupera el valor de la celda ReflectionDist desde la definición de tema.  <br/> |
|"ReflectionSize"  <br/> |Recupera el valor de la celda ReflectionSize desde la definición de tema.  <br/> |
|"ReflectionTrans"  <br/> |Recupera el valor de la celda ReflectionTrans desde la definición de tema.  <br/> |
|"SoftEdgesSize"  <br/> |Recupera el valor de la celda SoftEdgesSize desde la definición de tema.  <br/> |
|"GlowSize"  <br/> |Recupera el valor de la celda GlowSize desde la definición de tema.  <br/> |
|"GlowColor"  <br/> |Recupera el valor de la celda GlowColor desde la definición de tema.  <br/> |
|"GlowTransparency"  <br/> |Recupera el valor de la celda GlowColorTrans desde la definición de tema.  <br/> |
|"SketchAmount"  <br/> |Recupera el valor de la celda SketchAmount desde la definición de tema.  <br/> |
|"SketchEnabled"  <br/> |Recupera el valor de la celda SketchEnabled desde la definición de tema.  <br/> |
|"SketchFillChange"  <br/> |Recupera el valor de la celda SketchFillChange desde la definición de tema.  <br/> |
|"SketchLineChange"  <br/> |Recupera el valor de la celda SketchLineChange desde la definición de tema.  <br/> |
|"SketchLineWeight"  <br/> |Recupera el valor de la celda SketchLineWeight desde la definición de tema.  <br/> |
|"LatinFont"  <br/> |Recupera el valor de la celda fuente de la definición de tema.  <br/> |
|"TextColor"  <br/> |Recupera el valor de la celda Color de la definición del tema.  <br/> |
|"TextStyle"  <br/> |Recupera el valor de la celda Character.Style de la definición del tema.  <br/> |
|"ComplexFont"  <br/> |Recupera el valor de la celda ComplexScriptFont de la definición del tema.  <br/> |
|"AsianFont"  <br/> |Recupera el valor de la celda AsianFont de la definición del tema.  <br/> |
|"Color FillStop [x]"  <br/> |Recupera el valor de celda de Color de fila *x* de la definición del tema.  <br/> |
|"Transparencia FillStop [x]"  <br/> |Recupera el valor de celda de ColorTrans en fila *x* de la definición de tema.  <br/> |
|"Posición FillStop [x]"  <br/> |Recupera el valor de celda de la posición de fila *x* de la definición del tema.  <br/> |
|"Color LineStop [x]"  <br/> |Recupera el valor de celda de Color de fila *x* de la definición del tema.  <br/> |
|"Transparencia LineStop [x]"  <br/> |Recupera el valor de celda de ColorTrans en fila *x* de la definición de tema.  <br/> |
|"Posición LineStop [x]"  <br/> |Recupera el valor de celda de la posición de fila *x* de la definición del tema.  <br/> |
   
## <a name="example"></a>Ejemplo

 `THEMEVAL("5")`
  
Devuelve el color de "Énfasis 3" de la definición del tema.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Devuelve el valor de la celda "LineWeight" de la definición del tema. Si la forma que contiene esta función tiene sin tema que se ha aplicado, la función devuelve '0,7 pt.'.
  

