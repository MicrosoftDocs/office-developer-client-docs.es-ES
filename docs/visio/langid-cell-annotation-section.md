---
title: Celda LangID (Sección de anotación)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Indica el idioma del comentario.
ms.openlocfilehash: b3b2cba3d0a04f75ef2d87f0ee8dcd1f8115e15e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360553"
---
# <a name="langid-cell-annotation-section"></a>Celda LangID (sección de anotación)

Indica el idioma del comentario.
  
> [!NOTE]
> Esta celda se utiliza para realizar un seguimiento de los comentarios sólo cuando se abre un archivo. VSD en Microsoft Visio 2013 o cuando se guarda un archivo. vsdx en el formato de archivo. VSD. No se usa para el seguimiento de comentarios en documentos. vsdx en Visio 2013. 
  
## <a name="remarks"></a>Comentarios

Este valor es el identificador de configuración regional del idioma que se encuentra activo en la barra de idioma en el momento de la creación del comentario. Para obtener una lista de los idiomas admitidos por las aplicaciones de Microsoft Office, vea el tema sobre la celda [DocLangID](doclangid-cell-document-properties-section.md) (sección sobre propiedades del documento). 
  
Para obtener una referencia a la celda LangID por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Annotation. LangID [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia a la celda LangID por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionAnnotation** <br/> |
| Índice de fila:  <br/> |**visRowAnnotation** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visAnnotationLangID** <br/> |
   

