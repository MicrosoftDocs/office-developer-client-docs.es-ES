---
title: Celda CenterY (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Determina si la página de dibujo está centrada verticalmente en la página de la impresora.
ms.openlocfilehash: 2fde1d6301d7b9de4540cd12f21e5af01d7a6239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821774"
---
# <a name="centery-cell-print-properties-section"></a>Celda CenterY (sección Propiedades de impresión)

Determina si la página de dibujo está centrada verticalmente en la página de la impresora. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | La página de dibujo se centra verticalmente en la página de la impresora.  <br/> |
| FALSE  <br/> | La página de dibujo no se centra verticalmente en la página de la impresora (valor predeterminado).  <br/> |
   
## <a name="remarks"></a>Comentarios

De forma predeterminada, las páginas de dibujo están alineadas a la parte superior y a la izquierda de la página de la impresora. Si se establece el valor de las celdas CenterX y CenterY en TRUE, la página de dibujo se colocará en el centro de la página de la impresora (o páginas cuando sea necesario aplicar mosaico). 
  
Para obtener una referencia a la celda CenterY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | CenterY  <br/> |
   
Para obtener una referencia desde un programa a la celda CenterY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
| Índice de celda:  <br/> |**visPrintPropertiesCenterY** <br/> |
   

