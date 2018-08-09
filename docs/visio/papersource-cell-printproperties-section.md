---
title: Celda PaperSource (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Determina el origen del papel para la página.
ms.openlocfilehash: f1dedf210dfe0dd8cac3d36fdec03fb497f6572c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822724"
---
# <a name="papersource-cell-printproperties-section"></a>Celda PaperSource (sección Propiedades de impresión)

Determina el origen del papel para la página. 
  
## <a name="remarks"></a>Observaciones

Esta opción corresponde a la opción **Origen del papel** del cuadro de diálogo **Configurar impresión** (en el menú **Archivo**, haga clic en la flecha de **Configurar página** y, a continuación, en la ficha **Configurar impresión**, haga clic en el botón **Configurar**).
  
Los valores numéricos de esta celda están asignados a constantes (prefijadas por DMBIN) definidos para selecciones en el archivo wingdi.h de Microsoft Windows; Por ejemplo, el valor 7 representa a DMBIN_AUTO. 
  
Para obtener una referencia a la celda PaperSource por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |PaperSource  <br/> |
   
Para obtener una referencia desde un programa a la celda PaperSource por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
|Índice de celda:  <br/> |**visPrintPropertiesPaperSource** <br/> |
   

