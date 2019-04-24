---
title: Celda Rounding (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Indica el radio del arco de redondeo aplicado donde se unen dos segmentos contiguos de un trazado. Por ejemplo, el redondeo puede utilizarse para aplicar esquinas redondeadas a un rectángulo. Para establecer el redondeo, escriba un valor con unidades de medida (un par número-unidad).
ms.openlocfilehash: d64d3266e3dd2b0a3998955efe271aab04905fbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358586"
---
# <a name="rounding-cell-line-format-section"></a>Celda Rounding (Sección de formato de línea)

Indica el radio del arco de redondeo aplicado donde se unen dos segmentos contiguos de un trazado. Por ejemplo, el redondeo puede utilizarse para aplicar esquinas redondeadas a un rectángulo. Para establecer el redondeo, escriba un valor con unidades de medida (un par número-unidad).
  
## <a name="remarks"></a>Comentarios

También puede establecer este valor en el cuadro de diálogo **línea** (en la ficha **Inicio** , en el grupo **forma** , haga clic en **línea**, seleccione **grosor**y, a continuación, haga clic en **más líneas**).
  
Para obtener una referencia a la celda Rounding por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Rounding  <br/> |
   
Para obtener una referencia desde un programa a la celda Rounding por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLine** <br/> |
|Índice de celda:  <br/> |**visLineRounding** <br/> |
   

