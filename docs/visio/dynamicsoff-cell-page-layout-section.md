---
title: Celda DynamicsOff (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Determina si las formas colocables se mueven y los conectores cambian sus recorridos para evitar a las restantes formas y conectores de la página de dibujo.
ms.openlocfilehash: 72d65860d1a2ee37efd5287ae3f4baf54bd3addb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822042"
---
# <a name="dynamicsoff-cell-page-layout-section"></a>Celda DynamicsOff (sección Diseño de página)

Determina si las formas colocables se mueven y los conectores cambian sus recorridos para evitar a las restantes formas y conectores de la página de dibujo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | Deshabilitar propiedades dinámicas.  <br/> |
| FALSE  <br/> | Habilitar propiedades dinámicas.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede deshabilitar las propiedades dinámicas para mejorar el rendimiento de la solución. Por ejemplo, si una solución agrega formas colocables a un dibujo y no desea que la aplicación cambie las rutas de los conectores y las posiciones de las formas cada vez que se agregue una, puede deshabilitar las propiedades dinámicas. Vuelva a habilitarlas cuando la solución haya agregado las formas.
  
Para obtener una referencia a la celda DynamicsOff por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | DynamicsOff  <br/> |
   
Para obtener una referencia desde un programa a la celda DynamicsOff por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPageLayout** <br/> |
| Índice de celda:  <br/> |**visPLODynamicsOff** <br/> |
   

