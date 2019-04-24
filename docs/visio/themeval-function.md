---
title: Función THEMEVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: Recupera los valores del tema activo.
ms.openlocfilehash: ba95b8a920174ee44c0349d7227258d3ee8a843c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326687"
---
# <a name="themeval-function"></a>Función THEMEVAL

Recupera los valores del tema activo. 
  
## <a name="version-information"></a>Información de versiones

Versión añadida: Visio 2013
 
  
## <a name="syntax"></a>Sintaxis

 **THEMEVAL** ([ _"theme_value"_] [, _predeterminado_]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _"theme_value"_ <br/> |Opcional  <br/> |**String** <br/> |Nombre de una celda de la definición del tema del que se va a obtener un valor.  <br/> |
| _default_ <br/> |Opcional  <br/> |Varios  <br/> |Un valor predeterminado si el documento no tiene temas (no hay ninguna definición de tema).  <br/> |
   
## <a name="remarks"></a>Comentarios

Si la función **THEMEVAL** no recibe ningún argumento, devuelve el valor con temas de la celda host. Este es el valor que se almacena en la definición del tema actual. La celda host debe tener la misma capacidad para devolver un valor; Si la celda no puede ser con temas, **THEMEVAL** devuelve un error. 
  
Si la función **THEMEVAL** recibe un único argumento, recupera el valor de la definición del tema que se pasa como argumento. El argumento que se pasa para el primer parámetro debe ser un entero o una de las cadenas exactas que aparecen en la tabla siguiente. 
  
La función **THEMEVAL** también puede aceptar un entero para el primer parámetro, como un valor entre 1 y 8. El uso de valores enteros recupera un color por su índice de la combinación de colores del tema. Por lo tanto, un valor de ' 1 ' devolverá el color "oscuro" del tema, ' 2 ' devuelve el color "Light", ' 3 ' devuelve el color "énfasis 1", etc. 
  
Si la función **THEMEVAL** recibe dos argumentos, recupera el valor de la definición del tema que se pasa como primer argumento. Sin embargo, si el documento no tiene ningún tema aplicado, la función **THEMEVAL** usa el valor especificado como segundo argumento. 
  
**Posibles argumentos para el parámetro "theme_value"**

|**Value**|**Descripción**|
|:-----|:-----|
|Púrpura  <br/> |Recupera el color RGB oscuro de la definición del tema.  <br/> |
|Delgada  <br/> |Recupera el color RGB claro de la definición del tema.  <br/> |
|BackgroundColor  <br/> |Recupera el color RGB de fondo de la definición del tema.  <br/> |
|"AccentColor"  <br/> |Recupera el color RGB Accent1 de la definición del tema.  <br/> |
|"AccentColor2"  <br/> |Recupera el color RGB Accent2 de la definición del tema.  <br/> |
|"AccentColor3"  <br/> |Recupera el color RGB Accent3 de la definición del tema.  <br/> |
|"AccentColor4"  <br/> |Recupera el color RGB Accent4 de la definición del tema.  <br/> |
|"AccentColor5"  <br/> |Recupera el color RGB Accent5 de la definición del tema.  <br/> |
|"AccentColor6"  <br/> |Recupera el color RGB Accent6 de la definición del tema.  <br/> |
|LinePattern  <br/> |Recupera el valor de celda LinePattern de la definición del tema.  <br/> |
|LineWeight  <br/> |Recupera el valor de la celda LineWeight de la definición del tema.  <br/> |
|LineColor  <br/> |Recupera el valor de celda LineColor de la definición del tema.  <br/> |
|LineCap  <br/> |Recupera el valor de la celda LineCap de la definición del tema.  <br/> |
|"LineBegin"  <br/> |Recupera el valor de celda BeginArrow de la definición del tema.  <br/> |
|"LineEnd"  <br/> |Recupera el valor de la celda endArrow de la definición del tema.  <br/> |
|LineColorTrans  <br/> |Recupera el valor de Celda LineColorTrans de la definición del tema.  <br/> |
|"LineCompoundtype"  <br/> |Recupera el valor de la celda CompoundType de la definición del tema.  <br/> |
|"LineBegin"  <br/> |Recupera el valor de celda BeginArrow de la definición del tema.  <br/> |
|"LineEnd"  <br/> |Recupera el valor de la celda endArrow de la definición del tema.  <br/> |
|"LineBeginSize"  <br/> |Recupera el valor de celda BeginArrowSize de la definición del tema.  <br/> |
|"LineEndSize"  <br/> |Recupera el valor de la celda EndArrowSize de la definición del tema.  <br/> |
|"LineRounding"  <br/> |Recupera el valor de la celda de redondeo de la definición del tema.  <br/> |
|"ConnectorColor"  <br/> |Recupera el valor de celda LineColor de la definición del tema.  <br/> |
|"ConnectorPattern"  <br/> |Recupera el valor de celda LinePattern de la definición del tema.  <br/> |
|"ConnectorWeight"  <br/> |Recupera el valor de la celda LineWeight de la definición del tema.  <br/> |
|"ConnectorTransparency"  <br/> |Recupera el valor de Celda LineColorTrans de la definición del tema.  <br/> |
|"ConnectorRounding"  <br/> |Recupera el valor de la celda de redondeo de la definición del tema.  <br/> |
|"ConnectorBegin"  <br/> |Recupera el valor de celda BeginArrow de la definición del tema.  <br/> |
|Connectorenddebe  <br/> |Recupera el valor de la celda endArrow de la definición del tema.  <br/> |
|"ConnectorBeginSize"  <br/> |Recupera el valor de celda BeginArrowSize de la definición del tema.  <br/> |
|"ConnectorEndSize"  <br/> |Recupera el valor de la celda EndArrowSize de la definición del tema.  <br/> |
|FillColor  <br/> |Recupera el valor de celda FillForegnd de la definición del tema.  <br/> |
|"FillColor2"  <br/> |Recupera el valor de celda FillBkgnd de la definición del tema.  <br/> |
|"FillTransparency"  <br/> |Recupera el valor de celda FillForegndTrans de la definición del tema.  <br/> |
|FillPattern  <br/> |Recupera el valor de celda FillPattern de la definición de tema.  <br/> |
|LineGradientEnabled  <br/> |Recupera el valor de la celda LineGradientEnabled de la definición del tema.  <br/> |
|LineGradientDir  <br/> |Recupera el valor de la celda LineGradientDir de la definición del tema.  <br/> |
|LineGradientAngle  <br/> |Recupera el valor de la celda LineGradientAngle de la definición del tema.  <br/> |
|FillGradientEnabled  <br/> |Recupera el valor de la celda FillGradientEnabled de la definición del tema.  <br/> |
|FillGradientDir  <br/> |Recupera el valor de la celda FillGradientDir de la definición del tema.  <br/> |
|FillGradientAngle  <br/> |Recupera el valor de la celda FillGradientAngle de la definición del tema.  <br/> |
|RotateGradientWithShape  <br/> |Recupera el valor de la celda RotateGradientWithShape de la definición del tema.  <br/> |
|UseGroupGradient  <br/> |Recupera el valor de la celda UseGroupGradient de la definición del tema.  <br/> |
|"ShadowType"  <br/> |Recupera el valor de celda ShapeShdwType de la definición del tema.  <br/> |
|"ShadowColor"  <br/> |Recupera el valor de la celda ShdwColor de la definición del tema.  <br/> |
|"ShadowTransparency"  <br/> |Recupera el valor de la celda ShdwColorTrans de la definición del tema.  <br/> |
|"ShadowMagnification"  <br/> |Recupera el valor de celda ShapeShdwScaleFactor de la definición de tema.  <br/> |
|"ShadowBlur"  <br/> |Recupera el valor de la celda ShapeShdwBlur de la definición del tema.  <br/> |
|"ShadowXOffset"  <br/> |Recupera el valor de celda ShapeShdwOffsetX de la definición de tema.  <br/> |
|"ShadowYOffset"  <br/> |Recupera el valor de celda ShapeShdwOffsetY de la definición del tema.  <br/> |
|"ShadowDirection"  <br/> |Recupera el valor de celda ShapeShdwObliqueAngle de la definición del tema.  <br/> |
|"ShadowPattern"  <br/> |Recupera el valor de celda ShdwPattern de la definición del tema.  <br/> |
|BevelTopType  <br/> |Recupera el valor de la celda BevelTopType de la definición del tema.  <br/> |
|BevelTopWidth  <br/> |Recupera el valor de la celda BevelTopWidth de la definición del tema.  <br/> |
|BevelTopHeight  <br/> |Recupera el valor de la celda BevelTopHeight de la definición del tema.  <br/> |
|"BevelMaterial"  <br/> |Recupera el valor de la celda BevelMaterialType de la definición del tema.  <br/> |
|"BevelLighting"  <br/> |Recupera el valor de la celda BevelLightingType de la definición del tema.  <br/> |
|BevelLightingAngle  <br/> |Recupera el valor de la celda BevelLightingAngle de la definición del tema.  <br/> |
|BevelContourColor  <br/> |Recupera el valor de la celda BevelContourColor de la definición del tema.  <br/> |
|BevelContourSize  <br/> |Recupera el valor de la celda BevelContourSize de la definición del tema.  <br/> |
|ReflectionBlur  <br/> |Recupera el valor de la celda ReflectionBlur de la definición del tema.  <br/> |
|ReflectionDist  <br/> |Recupera el valor de la celda ReflectionDist de la definición del tema.  <br/> |
|ReflectionSize  <br/> |Recupera el valor de la celda reFlection de la definición del tema.  <br/> |
|ReflectionTrans  <br/> |Recupera el valor de la celda ReflectionTrans de la definición del tema.  <br/> |
|SoftEdgesSize  <br/> |Recupera el valor de la celda SoftEdgesSize de la definición del tema.  <br/> |
|GlowSize  <br/> |Recupera el valor de la celda GlowSize de la definición del tema.  <br/> |
|GlowColor  <br/> |Recupera el valor de la celda GlowColor de la definición del tema.  <br/> |
|"GlowTransparency"  <br/> |Recupera el valor de la celda GlowColorTrans de la definición del tema.  <br/> |
|SketchAmount  <br/> |Recupera el valor de la celda SketchAmount de la definición del tema.  <br/> |
|SketchEnabled  <br/> |Recupera el valor de la celda SketchEnabled de la definición del tema.  <br/> |
|SketchFillChange  <br/> |Recupera el valor de la celda SketchFillChange de la definición del tema.  <br/> |
|SketchLineChange  <br/> |Recupera el valor de la celda SketchLineChange de la definición del tema.  <br/> |
|SketchLineWeight  <br/> |Recupera el valor de la celda SketchLineWeight de la definición del tema.  <br/> |
|"LatinFont"  <br/> |Recupera el valor de la celda Font de la definición del tema.  <br/> |
|TextColor  <br/> |Recupera el valor de la celda de color de la definición del tema.  <br/> |
|Estilo  <br/> |Recupera el valor de la celda character. Style de la definición del tema.  <br/> |
|"ComplexFont"  <br/> |Recupera el valor de celda ComplexScriptFont de la definición del tema.  <br/> |
|AsianFont  <br/> |Recupera el valor de celda AsianFont de la definición del tema.  <br/> |
|"FillStop [x] color"  <br/> |Recupera el valor de la celda color en la fila *x* de la definición del tema.  <br/> |
|"FillStop [x] transparencia"  <br/> |Recupera el valor de la celda ColorTrans de la fila *x* de la definición del tema.  <br/> |
|"FillStop [x] posición"  <br/> |Recupera el valor de la celda Position de la fila *x* de la definición del tema.  <br/> |
|"LineStop [x] color"  <br/> |Recupera el valor de la celda color en la fila *x* de la definición del tema.  <br/> |
|"LineStop [x] transparencia"  <br/> |Recupera el valor de la celda ColorTrans de la fila *x* de la definición del tema.  <br/> |
|"LineStop [x] posición"  <br/> |Recupera el valor de la celda Position de la fila *x* de la definición del tema.  <br/> |
   
## <a name="example"></a>Ejemplo

 `THEMEVAL("5")`
  
Devuelve el color "acentuado 3" de la definición del tema.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Devuelve el valor de la celda "LineWeight" de la definición del tema. Si la forma que contiene esta función no tiene ningún tema aplicado, la función devuelve ' 0,7 PTO. '.
  

