---
title: Celda WalkPreference (Sección de información de pegado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
localization_priority: Normal
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: Determina si un extremo de una forma 1D se mueve a un punto de conexión horizontal o vertical de la forma a la que se pega, cuando se usa pegado dinámico y la forma se mueve a una posición ambigua. De forma predeterminada, ambos extremos de la forma 1D se mueven a los puntos de conexión horizontales.
ms.openlocfilehash: 05f7ded3f7336dc2f8598e8d1e9edc501b511546
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408610"
---
# <a name="walkpreference-cell-glue-info-section"></a>Celda WalkPreference (Sección de información de pegado)

Determina si un extremo de una forma 1D se mueve a un punto de conexión horizontal o vertical de la forma a la que se pega, cuando se usa pegado dinámico y la forma se mueve a una posición ambigua. De forma predeterminada, ambos extremos de la forma 1D se mueven a los puntos de conexión horizontales.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 1  <br/> | El punto inicial de la forma 1D se mueve a un punto de conexión vertical y el extremo se mueve a un punto de conexión horizontal (conexiones entre el borde superior y un lado, o entre el borde inferior y un lado).  <br/> |**visWalkPrefBegNS** <br/> |
| segundo  <br/> | El punto inicial de la forma 1D se mueve a un punto de conexión horizontal y el extremo se mueve a un punto de conexión vertical (conexiones entre un lado y el borde superior, o entre un lado y el borde inferior).  <br/> |**visWalkPrefEndNS** <br/> |
   
## <a name="remarks"></a>Comentarios

Esta celda no tiene ningún efecto en los conectores dinámicos. El comportamiento de los conectores dinámicos viene determinado por su estilo de enrutamiento. Vea la celda RouteStyle para ver el estilo de enrutamiento predeterminado para los conectores dinámicos de una página o la celda ShapeRouteStyle para ver el estilo de enrutamiento de un conector dinámico determinado.
  
Para obtener una referencia a la celda WalkPreference por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | WalkPreference  <br/> |
   
Para obtener una referencia desde un programa a la celda WalkPreference por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visWalkPref** <br/> |
   

