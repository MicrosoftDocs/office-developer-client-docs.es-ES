---
title: Celda ShdwScaleFactor (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Especifica el porcentaje para aumentar o reducir la forma de una sombra.
ms.openlocfilehash: 99bc48f5332830512e1f5c2f6d93c70b67197c03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823212"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>Celda ShdwScaleFactor (sección Propiedades de la página)

Especifica el porcentaje para aumentar o reducir la forma de una sombra. 
  
## <a name="remarks"></a>Observaciones

Cada sombra tiene una ubicación de eje sombreada, que es un punto de la sombra que corresponde al eje de la forma. Por ejemplo, si el eje de una forma se encuentra en el centro de la forma, la ubicación de eje sombreada sería el punto en el centro de la sombra. Cuando se aplica la escala a sombras simples, ampliación se centra en la ubicación de eje sombreada; Cuando se aplica la escala a sombras oblicuas, ampliación se aplica en la dirección oblicua. 
  
 Este porcentaje se utiliza cuando el tipo de sombra de una forma está establecido en el valor predeterminado de página (la celda ShapeShdwType es igual a ** visFSTPageDefault **). 
  
Para establecer este comportamiento para una forma individual, utilice la celda ShapeShdwScaleFactor de la sección de formato de relleno.
  
Este valor corresponde al del cuadro **Ampliación** de la ficha **Sombras** en el cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página**). 
  
Para obtener una referencia a la celda ShdwScaleFactor por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ShdwScaleFactor  <br/> |
   
Para obtener una referencia desde un programa a la celda ShdwScaleFactor por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageShdwScaleFactor** <br/> |
   

