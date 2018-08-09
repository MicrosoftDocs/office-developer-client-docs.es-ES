---
title: Celda LangID (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Indica el idioma de las fórmulas de celda.
ms.openlocfilehash: 669bde032daeda90b22cdab5d1758c6cbd4109d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822448"
---
# <a name="langid-cell-miscellaneous-section"></a>Celda LangID (sección Varios)

Indica el idioma de las fórmulas de celda. 
  
## <a name="remarks"></a>Comentarios

Para obtener una lista de los idiomas admitidos por las aplicaciones de Microsoft Office, vea el tema sobre la celda [DocLangID](doclangid-cell-document-properties-section.md) (sección sobre propiedades del documento). 
  
Para obtener una referencia a la celda LangID por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LangID  <br/> |
   
Para obtener una referencia a la celda LangID por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visObjLangID** <br/> |
   

