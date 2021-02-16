---
title: Celda LangID (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Indica el idioma del valor de los datos de formas.
ms.openlocfilehash: c5a0cca5f71bc5520337ad2bdcf354a2b4affe92
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420328"
---
# <a name="langid-cell-shape-data-section"></a>Celda LangID (Sección de datos de formas)

Indica el idioma del valor de los datos de formas. 
  
## <a name="remarks"></a>Comentarios

Para obtener una lista de los idiomas admitidos por las aplicaciones de Microsoft Office System, vea la celda [DocLangID](doclangid-cell-document-properties-section.md) (Sección de propiedades del documento). 
  
Para obtener una referencia a la celda LangID por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Prop.  *nombre*  . LangID donde Prop.  *nombre*  es el nombre de fila  <br/> |
   
Para obtener una referencia a la celda LangID por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionProp** <br/> |
| Índice de fila:  <br/> |**visRowProp**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCustPropsLangID** <br/> |
   

