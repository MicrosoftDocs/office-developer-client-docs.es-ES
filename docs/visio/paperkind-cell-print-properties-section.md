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
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408449"
---
# <a name="paperkind-cell-print-properties-section"></a>Celda PaperKind (sección de propiedades de impresión)

Especifica el tipo de papel donde imprimir la página.
  
## <a name="remarks"></a>Comentarios

Esta configuración corresponde  a la configuración  tamaño de papel en el cuadro  de diálogo Configurar impresión  (en la ficha Diseño, haga clic en la flecha de configuración de página y, a continuación, en la ficha Configurar impresión, haga clic en el botón **Configurar).**  
  
Los valores numéricos de esta celda se asignan a constantes (con el prefijo DMPAPER) definidas para las selecciones de papel en el archivo wingdi.h de Microsoft Windows. 
  
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
   

