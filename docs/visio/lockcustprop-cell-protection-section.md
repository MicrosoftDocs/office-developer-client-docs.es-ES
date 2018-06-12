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
description: Determina si el usuario puede agregar, eliminar o modificar datos de formas en la interfaz de usuario (UI) mediante el cuadro de diálogo Definir datos de formas o en el menú contextual de la ventana datos de formas.
ms.openlocfilehash: a88da9e4973f819b398b5bdeda434ede14640797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822506"
---
# <a name="lockcustprop-cell-protection-section"></a>Celda LockCustProp (Sección de protección)

Determina si el usuario puede agregar, eliminar o modificar datos de formas en la interfaz de usuario (UI) mediante el cuadro de diálogo **Definir datos de formas** o en el menú contextual de la ventana **Datos de formas** . 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El comando **Definir datos de formas** en el menú contextual en la ventana **Datos de formas** está deshabilitado.  <br/> |
|FALSE  <br/> |El comando **Definir datos de formas** en el menú contextual en la ventana **Datos de formas** está habilitado (valor predeterminado).  <br/> |
   
## <a name="remarks"></a>Observaciones

El valor TRUE no impide al usuario cambiar el valor de un elemento de datos de formas ni cambiar la sección de datos de formas de la ventana ShapeSheet. 
  
Para obtener una referencia a la celda LockCustProp por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LockCustProp  <br/> |
   
Para obtener una referencia a la celda LockCustProp por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLock** <br/> |
|Índice de celda:  <br/> |**visLockCustProp** <br/> |
   

