---
title: Celda NoLiveDynamics (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: Determina si una forma cambia de tamaño o gira dinámicamente a medida que el usuario trabaja con ella.
ms.openlocfilehash: 043571243fe3698561bee8632e7fd18db04c9330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822674"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a>Celda NoLiveDynamics (Sección de varios)

Determina si una forma cambia de tamaño o gira dinámicamente a medida que el usuario trabaja con ella.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | La forma no se actualiza dinámicamente mientras el usuario trabaja con ella.  <br/> |
| FALSE  <br/> | La forma se actualiza dinámicamente mientras el usuario trabaja con ella.  <br/> |
   
## <a name="remarks"></a>Comentarios

A medida que cambia de tamaño o gira una forma bidimensional (2D) sin dinámica activa, puede ver un cuadro de selección. Si la forma es unidimensional (1D), el efecto visual se basa en el valor de la celda DynFeedback.
  
Para obtener una referencia a la celda NoLiveDymanics por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | NoLiveDynamics  <br/> |
   
Para obtener una referencia a la celda NoLiveDynamics por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visNoLiveDynamics** <br/> |
   

