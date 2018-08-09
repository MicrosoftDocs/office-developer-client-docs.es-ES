---
title: Celda BegTrigger (Sección de información de pegado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm100
localization_priority: Normal
ms.assetid: 0b7ffe39-ee6c-71eb-355c-9bb4660260f1
description: Contiene una fórmula desencadenadora generada por la aplicación que determina si se mueve el punto inicial de una forma 1D para mantener su conexión con otra forma.
ms.openlocfilehash: 5dec179f1847c30c6ef563d866360b6dd31a1d88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821548"
---
# <a name="begtrigger-cell-glue-info-section"></a>Celda BegTrigger (sección Información de pegado)

Contiene una fórmula desencadenadora generada por la aplicación que determina si se mueve el punto inicial de una forma 1D para mantener su conexión con otra forma.
  
## <a name="remarks"></a>Comentarios

Cuando se pega una forma 1D a otra utilizando el pegado dinámico, la aplicación genera una fórmula que hace referencia a la celda EventXFMod de la otra forma. Al cambiar esa forma, Visio vuelve a calcular cualquier fórmula que haga referencia a su celda EventXFMod, incluida la fórmula en la celda BegTrigger. Otras fórmulas de la forma 1D hacen referencia a la celda BegTrigger y mueven el punto inicial de la forma 1D o alteran la forma según sea necesario.
  
Para obtener una referencia a la celda BegTrigger por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | BegTrigger  <br/> |
   
Para obtener una referencia desde un programa a la celda BegTrigger por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowGroup** <br/> |
| Índice de celda:  <br/> |**visBegTrigger** <br/> |
   

