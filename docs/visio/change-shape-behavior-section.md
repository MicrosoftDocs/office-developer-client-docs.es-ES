---
title: Sección cambiar comportamiento de forma
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Determina las propiedades que se transfieren desde la forma antigua a la nueva forma durante una operación de reemplazo. Los valores de las celdas de la sección cambiar comportamiento de forma de la forma de patrón del reemplazo se leen durante la operación de reemplazo de formas.
ms.openlocfilehash: 74519b27ab5b2b5bafc7c00010a65769061bf691
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418669"
---
# <a name="change-shape-behavior-section"></a>Sección cambiar comportamiento de forma

Determina las propiedades que se transfieren desde la forma antigua a la nueva forma durante una operación de reemplazo. Los valores de las celdas de la sección **cambiar comportamiento de forma** de la forma de patrón del reemplazo se leen durante la operación de reemplazo de formas. 
  
## <a name="remarks"></a>Comentarios

Al establecer las celdas en la sección **cambiar comportamiento de forma** , puede asegurarse de que determinadas propiedades de la forma de reemplazo permanecen sin cambios durante la operación de reemplazo. Las propiedades que no están protegidas se actualizan con los valores de la forma local de la forma antigua durante la operación. 
  
Puede cambiar la configuración del comportamiento de reemplazo de una forma de patrón editando la forma de patrón (en la ventana **formas** , haga clic con el botón secundario en la forma, elija **modificar patrón**y, a continuación, haga clic en **Editar forma de patrón**) y cambie los valores de la [ ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)y [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) en la hoja de cálculo del patrón. 
  
> [!NOTE]
> No puede cambiar el comportamiento de reemplazo de forma de las formas incluidas en las galerías de símbolos integradas en Microsoft Visio 2013. Para modificar el comportamiento de reemplazo de formas de las formas integradas de Visio, cree una nueva galería de símbolos y agregue la forma que desee modificar a la nueva galería de símbolos. 
  

