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
ms.openlocfilehash: b95dafda9ebef36db34f60585ab3ed2164ade415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822339"
---
# <a name="inhibitsnap-cell-page-properties-section"></a>Celda InhibitSnap (Sección de propiedades de página)

Determina si las formas de una página de primer plano se ajustan a otros objetos de esta página, así como a formas de una página de fondo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | Impide todo ajuste en la página, excepto el de la regla y la cuadrícula.  <br/> |
| FALSE  <br/> | Habilita el ajuste.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda InhibitSnap por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | InhibitSnap  <br/> |
   
Para obtener una referencia a la celda InhibitSnap por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageInhibitSnap** <br/> |
   

