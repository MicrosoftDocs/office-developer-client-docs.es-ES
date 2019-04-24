---
title: Celda GlueType (Sección de información de pegado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm420
localization_priority: Normal
ms.assetid: fffbefd6-8b0b-0023-6b03-026d1c6e885e
description: Determina si la forma 1D utiliza un pegado estático (punto a punto) o dinámico (forma a forma) cuando se pega encima de otra.
ms.openlocfilehash: ae4eddf17c6e7b5e56cb3397f03d0721d965c9b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339518"
---
# <a name="gluetype-cell-glue-info-section"></a>Celda GlueType (Sección de información de pegado)

Determina si la forma 1D utiliza un pegado estático (punto a punto) o dinámico (forma a forma) cuando se pega encima de otra.
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| &amp;H0  <br/> | Éste es el valor predeterminado. Permitir el pegado dinámico sólo para el conector dinámico y, si no es el caso, utilizar el pegado estático.  <br/> |**visGlueTypeDefault** <br/> |
| &amp;H1  <br/> | Permitir el pegado dinámico.  <br/> | Obsoleto en Visio 2002  <br/> |
| &amp;H2  <br/> | Permitir el pegado dinámico.  <br/> |**visGlueTypeWalking** <br/> |
| &amp;H4  <br/> | No permitir el pegado dinámico.  <br/> |**visGlueTypeNoWalking** <br/> |
| &amp;H8  <br/> | No permitir a esta forma bidimensional estar conectada con pegado dinámico.  <br/> |**visGlueTypeNoWalkingTo** <br/> |
   
## <a name="remarks"></a>Comentarios

Si la celda contiene un valor de 1, 2 o 3, el pegado dinámico determinará que acción de las siguientes acontecerá:
  
- Las formas tendrán un pegado dinámico en la interfaz de usuario.
    
- Las formas se pegarán en la celda PinX o PinY de otra forma de un programa.
    
El pegado estático se utilizará si las formas se pegan en otras celdas de la forma distintas de PinX y PinY en un programa.
  
Cambiar el valor de permitir a no permitir el pegado dinámico no anula ni modifica el pegado dinámico actual. Los programas pueden establecer el pegado dinámico aunque se haya deshabilitado en la celda GlueType.
  
Para obtener una referencia a la celda GlueType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | GlueType  <br/> |
   
Para obtener una referencia desde un programa a la celda GlueType por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visGlueType** <br/> |
   

