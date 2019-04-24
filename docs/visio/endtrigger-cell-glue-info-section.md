---
title: Celda EndTrigger (Sección de información de pegado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251331
localization_priority: Normal
ms.assetid: 8dc6515b-66ab-f1ac-18fd-820209f90991
description: Contiene una fórmula desencadenadora generada por la aplicación que determina si se mueve el extremo de una forma 1-D para mantener su conexión con otra forma.
ms.openlocfilehash: 9093cca782d9262b2511198ed73f512a75bb8994
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329067"
---
# <a name="endtrigger-cell-glue-info-section"></a>Celda EndTrigger (Sección de información de pegado)

Contiene una fórmula desencadenadora generada por la aplicación que determina si se mueve el extremo de una forma 1-D para mantener su conexión con otra forma.
  
## <a name="remarks"></a>Comentarios

Cuando se pega una forma 1-D a otra utilizando el pegado dinámico, Visio genera una fórmula que hace referencia a la celda EventXFMod de la otra forma. Al cambiar esa otra forma, Visio vuelve a calcular toda fórmula que se refiera a su celda EventXFMod, incluida la fórmula de la celda EndTrigger. Las demás fórmulas de la forma 1-D se remiten a la celda EndTrigger y mueven el extremo de la forma 1-D o la alteran según sea necesario.
  
Para obtener una referencia a la celda EndTrigger por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | EndTrigger  <br/> |
   
Para obtener una referencia desde un programa a la celda EndTrigger por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visEndTrigger** <br/> |
   

