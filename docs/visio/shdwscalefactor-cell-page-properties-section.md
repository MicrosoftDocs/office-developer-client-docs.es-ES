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
ms.openlocfilehash: 9175e9a1148779524fdce96ff18eac22fe8dd421
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429008"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>Celda ShdwScaleFactor (Sección de propiedades de página)

Especifica el porcentaje para aumentar o reducir la forma de una sombra. 
  
## <a name="remarks"></a>Comentarios

Cada sombra tiene una ubicación de eje sombreada, que es un punto en la sombra que corresponde al eje de la forma. Por ejemplo, si el eje de una forma se encuentra en el centro de ésta, la ubicación de eje sombreada sería el punto que se encuentra en el centro de la sombra. Al aplicar escala a sombras sencillas, la ampliación se centra en la ubicación de patillas sombreadas; al aplicar escala a sombras oblicuas, la ampliación se aplica en la dirección oblicua. 
  
 Este porcentaje se usa cuando el tipo de sombra de una forma se establece en Page Default (La celda ShapeShdwType es igual a ** visFSTPageDefault ** ). 
  
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
   

