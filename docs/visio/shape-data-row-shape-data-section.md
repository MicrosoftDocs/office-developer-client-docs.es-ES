---
title: Fila Data Row (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251344
localization_priority: Normal
ms.assetid: f3a83496-fccc-9d6a-02b9-60ebaf4911ea
description: Contiene la información de un único elemento de datos de formas asociado con una forma. Una forma contiene una fila Datos de formas para cada elemento de datos de formas.Las filas Datos de formas se denominan Prop.nombre y contienen las celdas siguientes. Para obtener más detalles, vea los temas de Ayuda acerca de la celda específica.
ms.openlocfilehash: 7bf7eafd1869aa3c3ee03efbde30560cdaaeb302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823129"
---
# <a name="shape-data-row-shape-data-section"></a>Fila Data Row (sección Datos de formas)

Contiene la información de un único elemento de datos de formas asociado con una forma. Una forma contiene una fila Datos de formas para cada elemento de datos de formas.Las filas Datos de formas se denominan Prop.nombre y contienen las celdas siguientes. Para obtener más detalles, vea los temas de Ayuda acerca de la celda específica.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[Label](label-cell-shape-data-section.md) <br/> |Especifica la etiqueta que ven los usuarios en el cuadro de diálogo o ventana **Datos de formas**.  <br/> |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |Especifica el texto descriptivo o las instrucciones que ven los usuarios en el cuadro de diálogo o ventana **Datos de formas** al seleccionar el elemento.  <br/> |
|[Tipo](type-cell-shape-data-section.md) <br/> |Especifica el tipo de datos para el valor del elemento de datos de formas: cadena (0), lista fija (1), número (2), valor booleano (3), lista variable (4), fecha u hora (5), duración (6) o moneda (7).  <br/> |
|[Formato](format-cell-shape-data-section.md) <br/> |Especifica el formato de un elemento de datos de formas.  <br/> |
|[Valor](value-cell-shape-data-section.md) <br/> |Contiene el valor del elemento tal y como se escribió en el cuadro de diálogo o ventana **Datos de formas**.  <br/> |
|[SortKey](sortkey-cell-shape-data-section.md) <br/> |Especifica la clave por la que se muestran los elementos en el cuadro de diálogo o ventana **Datos de formas**.  <br/> |
|[Invisible](invisible-cell-shape-data-section.md) <br/> |Especifica si el elemento de datos de formas es visible en el cuadro de diálogo o ventana **Datos de formas**. TRUE = no visible; FALSE = visible.<br/> |
|[Preguntar](ask-cell-shape-data-section.md) <br/> |Determina si se le pide al usuario que escriba información acerca de los datos de formas para una forma cuando crea una instancia o cuando duplica o copia la forma.  <br/> |
|[LangID](langid-cell-shape-data-section.md) <br/> |Especifica el idioma en el que se muestran los valores de los elementos de los datos de formas.  <br/> |
|[Calendario](calendar-cell-miscellaneous-section.md) <br/> |Especifica el tipo de calendario utilizado cuando el tipo de un elemento de datos de formas es Fecha.  <br/> |
   
## <a name="remarks"></a>Observaciones

 Puede agregar tantas filas Prop.  *nombre* como sea necesario, asignar nombres descriptivos a las filas y establecer valores de celda. Para agregar un elemento de datos de formas a una sección de datos de formas existente, haga clic en una fila y haga clic en **Insertar fila** en el menú contextual. 
  
Puede hacer referencia a estas celdas por su nombre de fila, que aparece en la ventana ShapeSheet en texto de color rojo. Para asignar nombres descriptivos a las filas Prop. *nombre* , haga clic en la fila y, a continuación, escriba un nombre como *precio* , por ejemplo, para crear el nombre de fila Prop.precio. A continuación, puede hacer referencia a la celda Label usando Prop.precio.Label. 
  
El nombre de fila que escriba debe ser único en la sección.
  

