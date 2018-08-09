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
ms.openlocfilehash: 0624ec42978292e84965c978d25e4052fc41613f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823017"
---
# <a name="rounding-cell-line-format-section"></a>Celda Rounding (sección Formato de línea)

Indica el radio del arco de redondeo aplicado donde se unen dos segmentos contiguos de un trazado. Por ejemplo, el redondeo puede utilizarse para aplicar esquinas redondeadas a un rectángulo. Para establecer el redondeo, escriba un valor con unidades de medida (un par número-unidad).
  
## <a name="remarks"></a>Observaciones

También puede establecer este valor en el cuadro de diálogo **línea** (en la ficha **Inicio** , en el grupo **forma** , haga clic en **línea**, elija **grosor**y, a continuación, haga clic en **Más líneas**).
  
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
   

