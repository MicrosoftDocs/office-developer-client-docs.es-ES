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
ms.openlocfilehash: dcb4a14ff89c7f5c77916e6b188aaf87e1711ab0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823496"
---
# <a name="uivisibility-cell-page-properties-section"></a>Celda UIVisibility (sección Propiedades de la página)

Determina si el nombre de la página está visible en la interfaz de usuario.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Muestra el nombre de la página en la interfaz de usuario (predeterminado).  <br/> |**visUIVNormal** <br/> |
|1  <br/> |No muestra el nombre de la página en la interfaz de usuario.  <br/> |**visUIVHidden** <br/> |
   
## <a name="remarks"></a>Comentarios

Si se establece la celda UIVisibility en **visUIVHidden** impide que la página aparezca en cualquier lugar en la interfaz de usuario donde aparece la cadena que contiene el nombre de la página. Por ejemplo, la página no se mostraría como una opción en el **Explorador de dibujos** o en las fichas de página. Sin embargo, la página sigue estando accesible, si utiliza las rutas de acceso de automatización o la interfaz de usuario que no incluya el nombre de la página, por ejemplo, el comando **Imprimir** . 
  
 Esta celda está concebida para usarse con páginas de documento, y no para páginas de superposición de revisiones, cuya celda UIVisibility está establecida en **visUIVHidden** de manera predeterminada y no debe cambiarse. 
  
> [!NOTE]
> Para ocultar una página del comando **Imprimir** del documento, convertirla en una página de fondo (la propiedad**Type** es **visTypeBackground** ) que no se usa como un fondo por ninguna página (las formas de fondo se imprimen páginas al es una página utilizando como un fondo imprime). Comando **Imprimir** del documento sólo funciona con páginas indizadas, y las páginas de fondo no se indizan. 
  
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
   

