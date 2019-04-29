---
title: Función ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Devuelve un valor Boolean que indica si una forma tiene un tema aplicado.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418123"
---
# <a name="isthemed-function"></a>Función ISTHEMED

Devuelve un valor Boolean que indica si una forma tiene un tema aplicado. 
  
## <a name="version-information"></a>Información de versiones

Versión añadida: Visio 2013
 
  
## <a name="syntax"></a>Sintaxis

 **ISTHEMED** ()
  
## <a name="return-value"></a>Valor devuelto

Booleano
  
## <a name="remarks"></a>Comentarios

> [!NOTE]
> La función **ISTHEMED** de Visio 2013 reemplaza la función **CELLISTHEMED** de versiones anteriores de Visio. 
  
La función **ISTHEMED** permite asignar las partes adecuadas del formato de un tema a una forma, pero mantener la capacidad de invalidar otras partes del formato del tema con un formato aplicado manualmente. Si, a continuación, vuelve a aplicar el tema, se reemplaza cualquier formato manual y la forma adopta todo el formato del tema. 
  
 **ISTHEMED** se evalúa como true si la celda [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) de la forma es mayor que 0. Si esta celda es igual a 0, **ISTHEMED** se evalúa como false. El tema de DocumentSheet y PageSheet no afectará al valor de la función **ISTHEMED** que se usa en ShapeSheet. Sólo si la función **ISTHEMED** se muestra en PageSheet es la cuestión del tema de la página. 
  
## <a name="example"></a>Ejemplo

||||
|:-----|:-----|:-----|
|Cell  <br/> |Fórmula  <br/> |Resultado  <br/> |
|Char. Font  <br/> |IF (ISTHEMED (), THEMEVAL (), FONT ("caLibri"))  <br/> |Si la forma tiene un tema aplicado, el texto de la forma acepta el formato de fuente del tema. Si la forma no tiene temas, el texto de la forma tiene el formato de la fuente "caLibri".  <br/> |
|LineColor  <br/> |SI (ISTHEMED, RGB (255, 0, 0), RGB (0, 255, 0))  <br/> |Si la forma tiene un temas aplicados, el color de la línea de la forma es rojo. Si la forma no tiene temas, el color de la línea de la forma es verde.  <br/> |
   

