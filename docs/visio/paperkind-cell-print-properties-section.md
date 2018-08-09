---
title: Celda PaperKind (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Especifica el tipo de papel donde imprimir la página.
ms.openlocfilehash: 03659553ab32afd20d1a5a40b85a8bbf107dbb08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822728"
---
# <a name="paperkind-cell-print-properties-section"></a>Celda PaperKind (sección Propiedades de impresión)

Especifica el tipo de papel donde imprimir la página.
  
## <a name="remarks"></a>Observaciones

Este valor corresponde a la configuración de **Tamaño de papel** en el cuadro de diálogo **Configurar impresión** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** y, a continuación, en la ficha **Configurar impresión** , haga clic en el botón **Configurar** ). 
  
Los valores numéricos de esta celda están asignados a constantes (prefijadas por DMPAPER) definen para selecciones de papel en el archivo wingdi.h de Microsoft Windows. 
  
Para obtener una referencia a la celda PaperKind por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |PaperKind  <br/> |
   
Para obtener una referencia desde un programa a la celda PaperKind por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
|Índice de celda:  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

