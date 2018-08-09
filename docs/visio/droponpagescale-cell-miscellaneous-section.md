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
ms.openlocfilehash: a586cca497e1ba04848142917a84c3aa8a25d081
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822026"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>Celda DropOnPageScale (sección Varios)

Contiene el porcentaje equivalente al cambio en la escala de la forma cuando se coloca en la página de dibujo.
  
## <a name="remarks"></a>Comentarios

En los dos siguientes casos, Visio cambia la escala de las formas de modo que aparezcan de forma adecuada en la página de dibujo:
  
- Cuando se colocan formas sin medir en dibujos a escala.
    
- Cuando se colocan formas medidas en dibujos sin escala.
    
El porcentaje de la celda DropOnPageScale indica el factor de escala la forma, una copia de seguridad de Visio (\>100) o hacia abajo (\<100). Puede utilizar este número como un factor al calcular valores codificado de forma rígida. 
  
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
   

