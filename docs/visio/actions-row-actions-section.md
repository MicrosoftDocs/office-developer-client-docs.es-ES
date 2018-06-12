---
title: Fila Actions (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60017
localization_priority: Normal
ms.assetid: 29a7464a-b9d4-a8ea-161b-3044de32ed23
description: Contiene celdas que especifican las acciones asociadas a un comando personalizado en un menú contextual o de acción de la etiqueta. La sección de acciones contiene una fila Actions por cada acción.
ms.openlocfilehash: f25ab75fe2bec35b09d2910ef731d11264224b7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821514"
---
# <a name="actions-row-actions-section"></a>Fila Actions (sección de acciones)

Contiene celdas que especifican las acciones asociadas a un comando personalizado en un menú contextual o de acción de la etiqueta. La sección de acciones contiene una fila Actions por cada acción.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
Las filas Actions se denominan Actions. *nombre* y contienen las celdas siguientes. Para obtener más información, vea los temas de la celda específica. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[Action](action-cell-actions-section.md) <br/> |Contiene la fórmula que se debe ejecutar cuando un usuario elige un elemento en un menú contextual o de acción de la etiqueta.  <br/> |
|[Menú](menu-cell-actions-section.md) <br/> |Define el nombre del elemento de menú que aparece en un menú contextual o de etiqueta de acción.  <br/> |
|[TagName](tagname-cell-actions-section.md) <br/> |Nombre lógico de la etiqueta de acción donde debe aparecer la acción.  <br/> |
|[ButtonFace](buttonface-cell-actions-section.md) <br/> |Identifica el icono que aparece junto a un elemento en un menú contextual o de etiquetas de acción.  <br/> |
|[SortKey](sortkey-cell-actions-section.md) <br/> |Número que determina el orden de los elementos de menú en un menú contextual o de etiquetas de acción.  <br/> |
|[Checked](checked-cell-actions-section.md) <br/> |Indica si el elemento de menú aparece activado en un menú contextual o de etiqueta de acción.  <br/> |
|[Deshabilitado](disabled-cell-actions-section.md) <br/> |Indica si un elemento de menú de un menú contextual o de etiquetas de acción está deshabilitado.  <br/> |
|[ReadOnly](readonly-cell-actions-section.md) <br/> |Indica si el elemento de menú es de sólo lectura (no se puede hacer clic en él).  <br/> |
|[Invisible](invisible-cell-actions-section.md) <br/> |Indica si el elemento de menú es visible en el menú contextual o de etiquetas de acción.  <br/> |
|[BeginGroup](begingroup-cell-actions-section.md) <br/> |Indica si se debe insertar un separador en el menú encima del elemento de menú.  <br/> |
   
## <a name="remarks"></a>Notas

 Puede agregar todas las acciones.  *nombre* como sea necesario, asignar nombres descriptivos a las filas y establecer valores de celda. Para agregar un comando personalizado a una sección de acciones ya existente, haga clic en una fila y haga clic en **Insertar fila** en el menú contextual. 
  
Puede hacer referencia a estas celdas por su nombre de fila, que aparece en la ventana ShapeSheet en texto de color rojo. Para asignar un nombre descriptivo a una de las acciones. *nombre de* fila, haga clic en la fila y, a continuación, escriba un nombre como *personalizada* , por ejemplo, para crear el nombre de fila Actions.personalizada. A continuación, puede hacer referencia a la celda Menu por Actions.descripción.Menu. 
  
El nombre de fila que escriba debe ser único en la sección.
  

