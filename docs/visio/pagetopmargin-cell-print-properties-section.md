---
title: Celda PageTopMargin (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
localization_priority: Normal
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: Especifica el margen superior de la página impresa.
ms.openlocfilehash: 1b7be63e3f21365231120c602d8edfe1dc727f88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822723"
---
# <a name="pagetopmargin-cell-print-properties-section"></a>Celda PageTopMargin (Sección de propiedades de impresión)

Especifica el margen superior de la página impresa.
  
## <a name="remarks"></a>Comentarios

Este valor representa unidades físicas y no se ve afectado por escalas ni unidades de dibujo. Por ejemplo, si esta celda tiene el valor 0,25 pda., este margen será de 0,25 pulgadas incluso si se utilizan pies como unidades en la página. Si las unidades no se indican explícitamente, este valor asume de forma predeterminada las unidades de la página. 
  
Para obtener una referencia a la celda PageTopMargin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageTopMargin  <br/> |
   
Para obtener una referencia a la celda PageTopMargin por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
| Índice de celda:  <br/> |**visPrintPropertiesTopMargin** <br/> |
   

