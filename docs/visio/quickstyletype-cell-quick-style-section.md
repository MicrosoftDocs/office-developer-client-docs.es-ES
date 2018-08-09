---
title: Celda QuickStyleType (sección Estilos rápidos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Determina el tipo de estilo rápido (dimensional 1, 2-dimensional o conector) que hereda de la forma.
ms.openlocfilehash: 211074800eee601d2658edbc03bb95d028920e54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822891"
---
# <a name="quickstyletype-cell-quick-style-section"></a>Celda QuickStyleType (sección Estilos rápidos)

Determina el tipo de estilo rápido (dimensional 1, 2-dimensional o conector) que hereda de la forma. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Visio elige automáticamente  <br/> |
|1  <br/> |1-dimensional  <br/> |
|2  <br/> |2-dimensional  <br/> |
|3  <br/> |Conector  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **QuickStyleType** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | QuickStyleType  <br/> |
   
Para obtener una referencia a la celda **QuickStyleType** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice de celda:  <br/> |**visQuickStyleType** <br/> |
   

