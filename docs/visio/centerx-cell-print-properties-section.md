---
title: Celda CenterX (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Determina si la página de dibujo está centrada horizontalmente en la página de la impresora.
ms.openlocfilehash: 13b05ed71248a3f8fada947fca6b203c6ab19c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418081"
---
# <a name="centerx-cell-print-properties-section"></a>Celda CenterX (Sección de propiedades de impresión)

Determina si la página de dibujo está centrada horizontalmente en la página de la impresora. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | La página de dibujo se centra horizontalmente en la página de la impresora.  <br/> |
| FALSE  <br/> | La página de dibujo no se centra horizontalmente en la página de la impresora (valor predeterminado).  <br/> |
   
## <a name="remarks"></a>Comentarios

De forma predeterminada, las páginas de dibujo están alineadas a la parte superior y a la izquierda de la página de la impresora. Si se establece el valor de las celdas CenterX y CenterY en TRUE, la página de dibujo se colocará en el centro de la página de la impresora (o páginas cuando sea necesario aplicar mosaico). 
  
Para obtener una referencia a la celda CenterX por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | CenterX  <br/> |
   
Para obtener una referencia desde un programa a la celda CenterX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
| Índice de celda:  <br/> |**visPrintPropertiesCenterX** <br/> |
   

