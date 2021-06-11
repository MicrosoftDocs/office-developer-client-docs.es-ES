---
title: Celda ExtraInfo (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Representa una cadena que pasa información que se utiliza en una dirección URL, como las coordenadas de un mapa de imagen. Por ejemplo, en la celda ExtraInfo, x=41 &amp; y=7 especifica las coordenadas de un mapa de imágenes.
ms.openlocfilehash: df2886ef7911b484cc60e8a476bfa53369fbf646
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409576"
---
# <a name="extrainfo-cell-hyperlinks-section"></a>Celda ExtraInfo (Sección de hipervínculos)

Representa una cadena que pasa información que se utiliza en una dirección URL, como las coordenadas de un mapa de imagen. Por ejemplo, en la celda ExtraInfo, "x=41 &amp; y=7" especifica las coordenadas de un mapa de imágenes.
  
## <a name="remarks"></a>Comentarios

Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.
  
Para obtener una referencia a la celda ExtraInfo por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Hipervínculo.  *nombre*  . ExtraInfo donde Hyperlink.  *nombre*  es el nombre de fila  <br/> |
   
Para obtener una referencia desde un programa a la celda ExtraInfo por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
| Índice de fila:  <br/> |**visRow1stHyperlink**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visHLinkExtraInfo** <br/> |
   

