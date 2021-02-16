---
title: Celda Ask (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Determina si se le pide al usuario que especifique los datos de formas cuando crea una instancia o cuando duplica o copia la forma.
ms.openlocfilehash: 0aa270ff918866d8f683a6408ccd71b6a22d555d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426868"
---
# <a name="ask-cell-shape-data-section"></a>Celda Ask (sección de datos de formas)

Determina si se le pide al usuario que especifique los datos de formas cuando crea una instancia o cuando duplica o copia la forma.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se pide al usuario que especifique los datos de formas en el cuadro de diálogo **Definir datos de formas**.  <br/> |
|FALSE  <br/> |No se le pide al usuario que especifique datos.  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta celda corresponde a la casilla **Preguntar al colocar** del cuadro de diálogo **Definir datos de formas** (haga clic con el botón secundario en la forma, seleccione **Datos** y, a continuación, en **Definir datos de formas**).
  
Para obtener una referencia a la celda Ask por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Prop. *nombre*  . Compruebe dónde prop.  *es*  el nombre de la fila de propiedad personalizada.  <br/> |
   
Para obtener una referencia a la celda Ask por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionProp** <br/> |
|Índice de fila:  <br/> |**visRowProp**  +   *i* donde *i* = 0, 1, 2,...  <br/> |
|Índice de celda:  <br/> |**visCustPropsAsk** <br/> |
   

