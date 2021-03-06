---
title: Celda Action (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Contiene la fórmula que se va a ejecutar cuando un usuario elige un comando en un menú contextual o de etiquetas de acción.
ms.openlocfilehash: e6bc576982cad871804cbcbc5f3d9c6bceb558c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407616"
---
# <a name="action-cell-actions-section"></a>Celda Action (sección de acciones)

Contiene la fórmula que se va a ejecutar cuando un usuario elige un comando en un menú contextual o de etiquetas de acción.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Comentarios

La celda Action se evalúa sólo cuando ocurre la acción, no al especificar la fórmula.
  
Para obtener una referencia a la celda Action por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Acciones.  *nombre*  . Acción donde acciones. *nombre*  es el nombre de la fila de acciones  <br/> |
   
Para obtener una referencia a la celda Action por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionAction** <br/> |
| Índice de fila:  <br/> |**visRowAction**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visActionAction** <br/> |
   

