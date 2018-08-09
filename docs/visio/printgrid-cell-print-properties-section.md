---
title: Celda PrintGrid (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Especifica si se imprime la cuadrícula al imprimir una página de documento.
ms.openlocfilehash: 76e5b5b4e82c39cbbffbecc710f05a77dbaa6332
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822879"
---
# <a name="printgrid-cell-print-properties-section"></a>Celda PrintGrid (sección Propiedades de impresión)

Especifica si se imprime la cuadrícula al imprimir una página de documento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Muestra la cuadrícula al imprimir esta página.  <br/> |
|FALSE  <br/> |No muestra la cuadrícula al imprimir esta página (predeterminado).  <br/> |
   
## <a name="remarks"></a>Observaciones

Este valor corresponde a la casilla **Cuadrícula** de la ficha **Configurar impresión** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página**). A excepción del color (se imprime en gris), la cuadrícula impresa coincide por completo con la que se ve en la ventana del dibujo de Microsoft Office Visio. 
  
Puede elegir si desea imprimir la cuadrícula de página por página. También puede definirse en una base de página por página en el estilo de la cuadrícula de la **regla &amp; cuadrícula** cuadro de diálogo (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ) cuando una página está activa. 
  
Para obtener una referencia a la celda PrintGrid por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |PrintGrid  <br/> |
   
Para obtener una referencia desde un programa a la celda PrintGrid por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
|Índice de celda:  <br/> |**visPrintPropertiesPrintGrid** <br/> |
   

