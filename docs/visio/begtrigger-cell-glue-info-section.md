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
ms.openlocfilehash: b401d349119337016a96b5fffbc26f7be2891864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360360"
---
# <a name="begtrigger-cell-glue-info-section"></a>Celda BegTrigger (Sección de información de pegado)

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
   

