---
title: Celda OnPage (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Indica si el dibujo se imprime en un número concreto de páginas de la impresora.
ms.openlocfilehash: 5b695ccf6fa2364809e2f5124b9f55ea6aab50e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822690"
---
# <a name="onpage-cell-print-properties-section"></a>Celda OnPage (Sección de propiedades de impresión)

Indica si el dibujo se imprime en un número concreto de páginas de la impresora. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Para ajustar la página de dibujo a un número establecido de páginas de la impresora.  <br/> |
|FALSE  <br/> |No ajusta la página de dibujo a un número establecido de páginas de la impresora (predeterminado).  <br/> |
   
## <a name="remarks"></a>Observaciones

Si la celda OnPage se establece en TRUE, Microsoft Visio recurrirá a las celdas PagesX y PagesY para determinar el número de páginas de impresora en que encajar el dibujo. Se omiten los valores de las celdas ScaleX y ScaleY. Esto puede considerarse una opción de escala automática.
  
Este valor corresponde a la opción **Ajustar a** en la ficha **Configurar impresión** en el cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** ). 
  
Para obtener una referencia a la celda OnPage por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |OnPage  <br/> |
   
Para obtener una referencia a la celda OnPage por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
|Índice de celda:  <br/> |**visPrintPropertiesOnPage** <br/> |
   

