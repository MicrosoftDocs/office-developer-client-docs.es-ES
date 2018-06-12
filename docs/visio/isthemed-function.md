---
title: ISTHEMED (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Devuelve un valor Boolean que indica si una forma tiene un tema que se ha aplicado.
ms.openlocfilehash: 4311780d8686b5792e999c204ec182d23efb723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822400"
---
# <a name="isthemed-function"></a>ISTHEMED (función)

Devuelve un valor Boolean que indica si una forma tiene un tema que se ha aplicado. 
  
## <a name="version-information"></a>Información de versión

Versión agregada: Visio 2013 
  
## <a name="syntax"></a>Sintaxis

 **ISTHEMED** ()
  
## <a name="return-value"></a>Valor devuelto

Boolean
  
## <a name="remarks"></a>Notas

> [!NOTE]
> La función **ISTHEMED** en Visio 2013 reemplaza la función **CELLISTHEMED** desde versiones anteriores de Visio. 
  
El **ISTHEMED** permite asignar las partes adecuadas del formato de un tema a una forma de funcionar pero conservar la posibilidad de reemplazar otras partes del tema formato con el formato aplicado manualmente. Si posteriormente se vuelve a aplicar el tema, cualquier formato manual se anula y la forma toma en todos los de formato del tema. 
  
 **ISTHEMED** se evalúa como TRUE si la celda [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) de la forma es mayor que 0. Si esta celda es igual a 0, **ISTHEMED** se evalúa como FALSE. El tema de la DocumentSheet y PageSheet no afecta al valor de la función **ISTHEMED** que se utiliza en una hoja ShapeSheet. Sólo si la función **ISTHEMED** se muestra en el PageSheet lo hace asunto del tema de la página. 
  
## <a name="example"></a>Ejemplo

||||
|:-----|:-----|:-----|
|Celda  <br/> |Fórmula  <br/> |Resultado  <br/> |
|Char.Font  <br/> |If(ISTHEMED(), THEMEVAL(), FONT("Calibri"))  <br/> |Si la forma tiene un estilo con que se ha aplicado, el texto de la forma acepta el formato del tema de fuente. Si la forma no es con temas, el texto de la forma tiene formato de la fuente "Calibri".  <br/> |
|LineColor  <br/> |IF (ISTHEMED, RGB (255, 0, 0), RGB (0, 255, 0))  <br/> |Si la forma tiene un estilo con que se ha aplicado, el color de línea de la forma es rojo. Si la forma no es con temas, el color de línea de la forma es de color verde.  <br/> |
   

