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
ms.openlocfilehash: eb6e7daccb1743c43a30b34598e47187496e4aac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406762"
---
# <a name="papersource-cell-printproperties-section"></a>Celda PaperSource (Sección de propiedades de impresión)

Determina el origen del papel para la página. 
  
## <a name="remarks"></a>Comentarios

Esta opción corresponde a la opción **Origen del papel** del cuadro de diálogo **Configurar impresión** (en el menú **Archivo**, haga clic en la flecha de **Configurar página** y, a continuación, en la ficha **Configurar impresión**, haga clic en el botón **Configurar**).
  
Los valores numéricos de esta celda se asignan a constantes (con el prefijo DMBIN) definidas para las selecciones de bin en el archivo wingdi.h de Microsoft Windows; por ejemplo, el valor 7 representa DMBIN_AUTO. 
  
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
   

