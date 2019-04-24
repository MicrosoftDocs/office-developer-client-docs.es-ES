---
title: Celda LockCustProp (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: Determina si el usuario puede agregar, eliminar o modificar datos de formas en la interfaz de usuario con el cuadro de diálogo Definir datos de formas o con el menú contextual de la ventana Datos de formas.
ms.openlocfilehash: 001123f3bd08d35f6f8e4874e20f2ee073835494
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359609"
---
# <a name="lockcustprop-cell-protection-section"></a>Celda LockCustProp (Sección de protección)

Determina si el usuario puede agregar, eliminar o modificar datos de formas en la interfaz de usuario con el cuadro de diálogo **Definir datos de formas** o con el menú contextual de la ventana **Datos de formas**. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El comando **Definir datos de formas** del menú contextual de la ventana **Datos de formas** está deshabilitado.  <br/> |
|FALSE  <br/> |El comando **Definir datos de formas** del menú contextual de la ventana **Datos de formas** está habilitado (de forma predeterminada).  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor TRUE no impide al usuario cambiar el valor de un elemento de datos de formas ni cambiar la sección de datos de formas de la ventana ShapeSheet. 
  
Para obtener una referencia a la celda LockCustProp por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LockCustProp  <br/> |
   
Para obtener una referencia desde un programa a la celda LockCustProp por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLock** <br/> |
|Índice de celda:  <br/> |**visLockCustProp** <br/> |
   

