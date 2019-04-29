---
title: Celda InhibitSnap (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Determina si las formas de una página de primer plano se ajustan a otros objetos de esta página, así como a formas de una página de fondo.
ms.openlocfilehash: 665130e9f9f938349028ffa1d1c06224e746de5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426754"
---
# <a name="inhibitsnap-cell-page-properties-section"></a>Celda InhibitSnap (Sección de propiedades de página)

Determina si las formas de una página de primer plano se ajustan a otros objetos de esta página, así como a formas de una página de fondo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | Impide todo ajuste en la página, excepto el de la regla y la cuadrícula.  <br/> |
| FALSE  <br/> | Habilita el ajuste.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda InhibitSnap por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | InhibitSnap  <br/> |
   
Para obtener una referencia a la celda InhibitSnap por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageInhibitSnap** <br/> |
   

