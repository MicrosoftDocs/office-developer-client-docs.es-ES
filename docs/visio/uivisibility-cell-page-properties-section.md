---
title: Celda UIVisibility (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Determina si el nombre de la página está visible en la interfaz de usuario.
ms.openlocfilehash: 51ccd34cb40c286fe6b61818aea5a6b9c0b6d1a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357221"
---
# <a name="uivisibility-cell-page-properties-section"></a>Celda UIVisibility (Sección de propiedades de página)

Determina si el nombre de la página está visible en la interfaz de usuario.
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Muestra el nombre de la página en la interfaz de usuario (predeterminado).  <br/> |**visUIVNormal** <br/> |
|1  <br/> |No muestra el nombre de la página en la interfaz de usuario.  <br/> |**visUIVHidden** <br/> |
   
## <a name="remarks"></a>Comentarios

Al establecer la celda UIVisibility como **visUIVHidden**, se impide que la página aparezca en cualquier lugar de la interfaz donde se muestra la cadena que contiene el nombre de la página. Por ejemplo, la página no se mostraría como opción en el cuadro de diálogo Página (menú Edición, submenú Ir a), en el **Explorador de dibujos** o en las fichas de la página. Sin embargo, la página sigue siendo accesible si usa rutas de interfaz de usuario o de automatización que no incluyen el nombre de la página, por ejemplo, el comando **Imprimir** . 
  
 Esta celda está concebida para usarse con páginas de documento, y no para páginas de superposición de revisiones, cuya celda UIVisibility está establecida en **visUIVHidden** de manera predeterminada y no debe cambiarse. 
  
> [!NOTE]
> Para ocultar una página del comando **Imprimir** del documento, debe convertirla en una página de fondo (la propiedad**Type** es **visTypeBackground** ) que no se usa como fondo por ninguna página (las formas de las páginas de fondo se imprimen cuando una página que la usa como fondo) impreso). El comando **Imprimir** del documento solo funciona con páginas indizadas y las páginas de fondo no se indizan. 
  
Para obtener una referencia a la celda UIVisibility por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |UIVisibility  <br/> |
   
Para obtener una referencia desde un programa a la celda UIVisibility por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPage** <br/> |
|Índice de celda:  <br/> |**visPageUIVisibility** <br/> |
   

