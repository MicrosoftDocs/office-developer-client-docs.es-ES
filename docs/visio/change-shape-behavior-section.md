---
title: Sección Cambiar comportamiento de forma
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Determina las propiedades que se transfieren durante una operación de reemplazo de la forma anterior a la forma de reemplazo. Los valores de las celdas en la sección cambiar el comportamiento de forma de patrón de la forma de la sustitución se leen durante la operación de reemplazo de forma.
ms.openlocfilehash: 3b4b3cac37b8415309a2433c19c2b420fd652df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821738"
---
# <a name="change-shape-behavior-section"></a>Sección Cambiar comportamiento de forma

Determina las propiedades que se transfieren durante una operación de reemplazo de la forma anterior a la forma de reemplazo. Los valores de las celdas en la sección **Comportamiento de cambio de forma** de patrón de la forma de la sustitución se leen durante la operación de reemplazo de forma. 
  
## <a name="remarks"></a>Comentarios

Mediante la configuración de las celdas en la sección **Comportamiento de cambio de forma** , puede asegurarse de que determinadas propiedades de la forma de sustitución no se modifican durante la operación de reemplazo. Las propiedades que no están protegidas se actualizan con los valores de forma local desde la antigua forma durante la operación. 
  
Puede cambiar la sustitución configuración del comportamiento de un patrón de forma mediante la edición el patrón de forma (en la ventana **formas** , haga clic en la forma, elija **Modificar patrón**y, a continuación, haga clic en **Modificar forma de patrón**) y cambiar los valores de la [ ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)y [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) las celdas de ShapeSheet del patrón. 
  
> [!NOTE]
> No se puede cambiar los comportamientos de sustitución de forma de las formas que se incluyen con las galerías de símbolos integrados en Microsoft Visio 2013. Para modificar los comportamientos de sustitución de forma de las formas de Visio integradas, cree una nueva galería de símbolos y agregue la forma que desee modificar la nueva galería de símbolos. 
  

