---
title: Sección Cambiar comportamiento de forma
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Determina las propiedades que se transfieren de la forma antigua a la forma de reemplazo durante una operación de reemplazo. Los valores de las celdas de la sección Cambiar comportamiento de forma de la forma maestra del reemplazo se leen durante la operación de reemplazo de formas.
ms.openlocfilehash: 74519b27ab5b2b5bafc7c00010a65769061bf691
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418669"
---
# <a name="change-shape-behavior-section"></a>Sección Cambiar comportamiento de forma

Determina las propiedades que se transfieren de la forma antigua a la forma de reemplazo durante una operación de reemplazo. Los valores de las celdas de la sección **Cambiar** comportamiento de forma de la forma maestra del reemplazo se leen durante la operación de reemplazo de formas. 
  
## <a name="remarks"></a>Comentarios

Al establecer las celdas en la sección **Cambiar** comportamiento de la forma, puede asegurarse de que determinadas propiedades de la forma de reemplazo no se modifiquen durante la operación de reemplazo. Las propiedades que no están protegidas se actualizan con los valores de forma local de la forma antigua durante la operación. 
  
Puede cambiar la configuración de comportamiento de reemplazo de una  forma Maestra editando la forma Maestra (en la ventana Formas, haga clic con el botón secundario en la forma, elija Editar patrón y, a continuación, haga clic en Editar forma **maestra)** y cambiando los valores de las [celdas ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)y [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) en la ShapeSheet del maestro. 
  
> [!NOTE]
> No puede cambiar los comportamientos de reemplazo de formas de las formas que se incluyen con las galerías de símbolos integradas en Microsoft Visio 2013. Para modificar los comportamientos de reemplazo de formas de las formas Visio integradas, cree una galería de símbolos nueva y agregue la forma que desea modificar a la nueva galería de símbolos. 
  

