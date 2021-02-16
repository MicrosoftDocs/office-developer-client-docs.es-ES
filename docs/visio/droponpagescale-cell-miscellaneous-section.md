---
title: Celda DropOnPageScale (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: 17c597df3d9e7e741d902fd566cc9a5de1f31ea0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423765"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>Celda DropOnPageScale (Sección de varios)

Contiene el porcentaje equivalente al cambio en la escala de la forma cuando se coloca en la página de dibujo.
  
## <a name="remarks"></a>Comentarios

En los dos siguientes casos, Visio cambia la escala de las formas de modo que aparezcan de forma adecuada en la página de dibujo:
  
- Cuando se colocan formas sin medir en dibujos a escala.
    
- Cuando las formas medidas se descartan en dibujos sin escala.
    
El porcentaje de la celda DropOnPageScale indica el factor por el que Visio escale la forma, ya sea hacia arriba ( \> 100) o hacia abajo ( \< 100). Esta cifra se puede usar como factor al calcular los valores que se encuentran en el código de software. 
  
El valor es el 100% para formas medidas en dibujos a escala y para formas sin medir en dibujos sin escala. 
  
Para obtener una referencia a la celda DropOnPageScale por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | DropOnPageScale  <br/> |
   
Para obtener una referencia desde un programa a la celda DropOnPageScale por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visObjDropOnPageScale** <br/> |
   

