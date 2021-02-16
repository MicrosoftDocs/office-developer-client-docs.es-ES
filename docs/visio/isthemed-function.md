---
title: Función ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Devuelve un valor booleano que indica si una forma tiene un tema aplicado.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418123"
---
# <a name="isthemed-function"></a>Función ISTHEMED

Devuelve un valor booleano que indica si una forma tiene un tema aplicado. 
  
## <a name="version-information"></a>Información de versiones

Versión añadida: Visio 2013
 
  
## <a name="syntax"></a>Sintaxis

 **ISTHEMED**()
  
## <a name="return-value"></a>Valor devuelto

Booleano
  
## <a name="remarks"></a>Comentarios

> [!NOTE]
> La **función ISTHEMED** de Visio 2013 reemplaza la función **CELLISTHEMED** de versiones anteriores de Visio. 
  
La **función ISTHEMED** permite asignar partes adecuadas del formato de un tema a una forma, pero conservar la capacidad de reemplazar otras partes del formato del tema con formato aplicado manualmente. Si posteriormente vuelve a aplicar el tema, se invalida cualquier formato manual y la forma toma todo el formato del tema. 
  
 **ISTHEMED se** evalúa como TRUE si la [celda ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) de la forma es mayor que 0. Si esta celda es igual a 0, **ISTHEMED** se evalúa como FALSE. El tema de DocumentSheet y PageSheet no afectará al valor de la función **ISTHEMED** usada en una ShapeSheet. Solo si la **función ISTHEMED** se muestra en pagesheet, el tema de la página es importante. 
  
## <a name="example"></a>Ejemplo

||||
|:-----|:-----|:-----|
|Cell  <br/> |Fórmula  <br/> |Resultado  <br/> |
|Char.Font  <br/> |IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))  <br/> |Si la forma tiene un tema aplicado, el texto de la forma acepta el formato de fuente del tema. Si la forma no tiene un formato, el texto de la forma tiene el formato de la fuente "Calibri".  <br/> |
|LineColor  <br/> |IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))  <br/> |Si la forma tiene un tema aplicado, el color de línea de la forma es rojo. Si la forma no tiene tema, el color de la línea de la forma es verde.  <br/> |
   

