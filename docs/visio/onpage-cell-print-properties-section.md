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
ms.openlocfilehash: 61d45a5bffdbb1afd5db9c608f80bc4f797f5191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439607"
---
# <a name="onpage-cell-print-properties-section"></a>Celda OnPage (Sección de propiedades de impresión)

Indica si el dibujo se imprime en un número concreto de páginas de la impresora. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Ajuste la página de dibujo a un número definido de páginas de impresora.  <br/> |
|FALSE  <br/> |No ajusta la página de dibujo a un número establecido de páginas de la impresora (predeterminado).  <br/> |
   
## <a name="remarks"></a>Comentarios

Si la celda OnPage se establece en TRUE, Microsoft Visio recurrirá a las celdas PagesX y PagesY para determinar el número de páginas de impresora en que encajar el dibujo. Se omiten los valores de las celdas ScaleX y ScaleY. Esto puede considerarse una opción de escala automática.
  
Este valor corresponde  a la opción  Ajustar a de la ficha Configurar  impresión del cuadro de diálogo Configurar página (en la ficha Diseño, haga clic en **la** flecha Configurar página).  
  
Para obtener una referencia a la celda OnPage por su nombre desde otra fórmula, o desde un programa mediante la **propiedad CellsU,** use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |OnPage  <br/> |
   
Para obtener una referencia desde un programa a la celda OnPage por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
|Índice de celda:  <br/> |**visPrintPropertiesOnPage** <br/> |
   

