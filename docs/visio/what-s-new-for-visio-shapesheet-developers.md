---
title: Novedades para programadores de ShapeSheet de Visio
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1046253
localization_priority: Normal
ms.assetid: d4f0cf7a-ac4b-c914-7887-e1d65e9d59fa
description: Visio 2013 proporciona una plataforma única eficaz para las soluciones de dibujo personalizadas. Las nuevas celdas y funciones ShapeSheet, junto con nuevos objetos de automatización, propiedades, métodos y eventos, le ofrecen más opciones para definir y controlar el comportamiento de los elementos de las soluciones.
ms.openlocfilehash: 9ab1c447e7cfdf41b8c88a85438ac2904b1395cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413328"
---
# <a name="whats-new-for-visio-shapesheet-developers"></a>Novedades para programadores de ShapeSheet de Visio

Visio 2013 proporciona una plataforma única eficaz para las soluciones de dibujo personalizadas. Las nuevas celdas y funciones ShapeSheet, junto con nuevos objetos de automatización, propiedades, métodos y eventos, le ofrecen más opciones para definir y controlar el comportamiento de los elementos de las soluciones.
  
## <a name="new-and-changed-cells"></a>Celdas nuevas y modificadas
<a name="vis15_WhatsNew_Cells"> </a>

En la tabla siguiente se enumeran las nuevas celdas que puede usar para crear soluciones ShapeSheet en Visio 2013.
  
|**Nueva celda**|**Section**|
|:-----|:-----|
|[BevelBottomHeight](bevelbottomheight-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[BevelBottomType](bevelbottomtype-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[BevelBottomWidth](bevelbottomwidth-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[BevelContourColor](bevelcontourcolor-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[BevelContourSize](bevelcontoursize-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[BevelDepthColor](beveldepthcolor-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[BevelDepthSize](beveldepthsize-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[BevelLightingAngle](bevellightingangle-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[BevelLightingType](bevellightingtype-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[BevelMaterialType](bevelmaterialtype-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[BevelTopHeight](beveltopheight-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[BevelTopType](beveltoptype-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[BevelTopWidth](beveltopwidth-cell-bevel-properties-section.md) <br/> |Propiedades biselado  <br/> |
|[ClippingPath](clippingpath-cell-foreign-image-info-section.md) <br/> |Información de imagen externa  <br/> |
|[ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) <br/> |Propiedades del tema  <br/> |
|[CompoundType](compoundtype-cell-line-format-section.md) <br/> |Formato de línea  <br/> |
|[ConnectorSchemeIndex](connectorschemeindex-cell-theme-properties-section.md) <br/> |Propiedades del tema  <br/> |
|[DistanceFromGround](distancefromground-cell-3-d-rotation-properties.md) <br/> |Propiedades de rotación 3D  <br/> |
|[DocLockReplace](doclockreplace-cell-document-properties-section.md) <br/> |Propiedades del documento  <br/> |
|[EffectSchemeIndex](effectschemeindex-cell-theme-properties-section.md) <br/> |Propiedades del tema  <br/> |
|[FillGradientAngle](fillgradientangle-cell-gradient-properties-section.md) <br/> |Propiedades de degradado  <br/> |
|[FillGradientDir](fillgradientdir-cell-gradient-properties-section.md) <br/> |Propiedades de degradado  <br/> |
|[FillGradientEnabled](fillgradientenabled-cell-gradient-properties-section.md) <br/> |Propiedades de degradado  <br/> |
|[FontSchemeIndex](fontschemeindex-cell-theme-properties-section.md) <br/> |Propiedades del tema  <br/> |
|[GlowColor](glowcolor-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[GlowColorTrans](glowcolortrans-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[GlowSize](glowsize-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[KeepTextFlat](keeptextflat-cell-3-d-rotation-properties-section.md) <br/> |Propiedades de rotación 3D  <br/> |
|[LineGradientAngle](linegradientangle-cell-gradient-properties-section.md) <br/> |Propiedades de degradado  <br/> |
|[LineGradientDir](linegradientdir-cell-gradient-properties-section.md) <br/> |Propiedades de degradado  <br/> |
|[LineGradientEnabled](linegradientenabled-cell-gradient-properties-section.md) <br/> |Propiedades de degradado  <br/> |
|[LockReplace](lockreplace-cell-protection-section.md) <br/> |Protección  <br/> |
|[LockThemeConnectors](lockthemeconnectors-cell-protection-section.md) <br/> |Protección  <br/> |
|[LockThemeFonts](lockthemefonts-cell-protection-section.md) <br/> |Protección  <br/> |
|[LockThemeIndex](lockthemeindex-cell-protection-section.md) <br/> |Protección  <br/> |
|[NoCoauth](nocoauth-cell-document-properties-section.md) <br/> |Propiedades del documento  <br/> |
|[PageLockReplace](pagelockreplace-cell-page-properties-section.md) <br/> |Propiedades de página  <br/> |
|[Perspective](perspective-cell-3-d-rotation-properties-section.md) <br/> |Propiedades de rotación 3D  <br/> |
|[QuickStyleEffectsMatrix](quickstyleeffectsmatrix-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleFillColor](quickstylefillcolor-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleFillMatrix](quickstylefillmatrix-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleFontColor](quickstylefontcolor-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleLineColor](quickstylelinecolor-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleLineMatrix](quickstylelinematrix-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleShadowColor](quickstyleshadowcolor-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleType](quickstyletype-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[ReflectionBlur](reflectionblur-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[ReflectionDist](reflectiondist-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[ReflectionSize](reflectionsize-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[ReflectionTrans](reflectiontrans-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md) <br/> |Cambiar comportamiento de la forma  <br/> |
|[ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md) <br/> |Cambiar comportamiento de la forma  <br/> |
|[ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md) <br/> |Cambiar comportamiento de la forma  <br/> |
|[ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) <br/> |Cambiar comportamiento de la forma  <br/> |
|[RotateGradientWithShape](rotategradientwithshape-cell-gradient-properties-section.md) <br/> |Propiedades de degradado  <br/> |
|[RotationType](rotationtype-cell-3-d-rotation-properties-section.md) <br/> |Propiedades de rotación 3D  <br/> |
|[RotationXAngle](rotationxangle-cell-3-d-rotation-properties-section.md) <br/> |Propiedades de rotación 3D  <br/> |
|[RotationYAngle](rotationyangle-cell-3-d-rotation-properties-section.md) <br/> |Propiedades de rotación 3D  <br/> |
|[RotationZAngle](rotationzangle-cell-3-d-rotation-properties-section.md) <br/> |Propiedades de rotación 3D  <br/> |
|[ShapeShdwBlur](shapeshdwblur-cell-fill-format-section.md) <br/> |Formato de relleno  <br/> |
|[ShapeShdwShow](shapeshdwshow-cell-fill-format-section.md) <br/> |Formato de relleno  <br/> |
|[SketchAmount](sketchamount-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[SketchEnabled](sketchenabled-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[SketchFillChange](sketchfillchange-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[SketchLineChange](sketchlinechange-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[SketchLineWeight](sketchlineweight-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[SketchSeed](sketchseed-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[SoftEdgesSize](softedgessize-cell-additional-effect-properties-section.md) <br/> |Propiedades de efecto adicionales  <br/> |
|[ThemeIndex](themeindex-cell-theme-properties-section.md) <br/> |Propiedades del tema  <br/> |
|[UseGroupGradient](usegroupgradient-cell-gradient-properties-section.md) <br/> |Propiedades de degradado  <br/> |
   
En la tabla siguiente se enumeran las celdas que se han cambiado en Visio 2013.
  
|**Celda modificada**|**Notas**|
|:-----|:-----|
|[ShdwType](shdwtype-cell-page-properties-section.md) <br/> |Nuevo valor y constante de automatización  <br/> |
   
## <a name="new-rows"></a>Nuevas filas
<a name="vis15_WhatsNew_Rows"> </a>

En la tabla siguiente se enumeran las nuevas filas que puede usar para crear soluciones ShapeSheet en Visio 2013.
  
|**Nueva fila**|**Section**|
|:-----|:-----|
|[GradientStop](gradient-stop-row-fill-gradient-section.md) <br/> |Degradado de relleno  <br/> |
|[GradientStop](gradient-stop-row-line-gradient-section.md) <br/> |Degradado de línea  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Geometría  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Geometría  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Geometría  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Geometría  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Geometría  <br/> |
   
## <a name="new-and-deprecated-functions"></a>Funciones nuevas y en desuso
<a name="vis15_WhatsNew_Functions"> </a>

En la tabla siguiente se enumeran las nuevas funciones de Visio 2013.
  
|**Nueva función**|
|:-----|
|[FONT](font-function.md) <br/> |
|[ISTHEMED](isthemed-function.md) <br/> |
|[LANGUAGE](language-function.md) <br/> |
|[THEMECBV](themecbv-function.md) <br/> |
||
|[THEMEVAL](themeval-function.md) <br/> |
   
En la tabla siguiente se enumeran las funciones en desuso Visio 2013.
  
|**Función en desuso**|**Notas**|
|:-----|:-----|
|**CELLISTHEMED** <br/> |Se reemplaza por [la función ISTHEMED.](isthemed-function.md)  <br/> |
   

