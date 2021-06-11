---
title: Crear tablas para mostrar y estructuras relacionadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 350272324c3827f4630f0cf35e3ade0ff213ac4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416247"
---
# <a name="creating-display-tables-and-related-structures"></a>Crear tablas para mostrar y estructuras relacionadas
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crear una tabla para mostrar es similar a escribir un programa con un lenguaje de scripting. Puede crear una tabla para mostrar llamando a [BuildDisplayTable](builddisplaytable.md) o escribiendo código personalizado para rellenar las filas y columnas de la tabla. En general, debe usar la **técnica BuildDisplayTable** porque es más sencilla. 
  
Antes de llamar a **BuildDisplayTable para** solicitar a MAPI que cree una tabla para mostrar, hay una jerarquía de estructuras que debe compilar. La estructura de nivel superior, [DTPAGE](dtpage.md), describe una sola página de propiedades con pestañas. En cada **estructura DTPAGE** hay una [estructura DTCTL](dtctl.md) que describe un único control, como un cuadro de edición o un botón de opción. Cada **estructura DTCTL** contiene una estructura específica del tipo de control. Por ejemplo, si la **estructura DTCTL** describe un control de cuadro de edición, contendrá una **estructura DTBLEDIT.** La **estructura DTCTL** de un botón de opción contiene una **estructura DTBLRADIOBUTTON.** 
  
Estas estructuras se relacionan directamente con **BuildDisplayTable**; no tienen ningún significado fuera del contexto de esta función. Cuando se llama **a BuildDisplayTable,** se pasan una o más estructuras **DTPAGE** como parámetros de entrada. Las **estructuras DTPAGE** contienen una matriz de estructuras **DTCTL** y un recuento del número de estructuras **DTCTL** en la matriz. Hay una estructura para que cada control se muestre en el cuadro de diálogo. **Las estructuras DTPAGE** también tienen una cadena de caracteres que representa el nombre de un archivo de ayuda y un recurso de cuadro de diálogo correspondientes. 
  
Cada **estructura DTCTL** de una **estructura DTPAGE** contiene los siguientes datos que se usan para establecer propiedades para el control: 
  
- Tipo de control para establecer **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)).
    
- Marcas de control para establecer **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
    
- Datos de notificación para establecer **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)).
    
- La estructura de control para **establecer PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).
    
**Las estructuras DTCTL** también contienen un identificador de recursos y, para los controles de edición y cuadro combinado, un filtro de caracteres. 
  
El miembro de la estructura de control de una **estructura DTCTL** describe los datos que son únicos para el tipo de control. MAPI define una estructura diferente para cada tipo de control. Por ejemplo, los datos de un control de edición se representan mediante una **estructura DTBLEDIT;** los datos de un cuadro de lista se representan mediante una **estructura DTBLLBX.** 
  
La relación entre los tres tipos de estructuras de tabla para mostrar se muestra en la siguiente ilustración. El cuadro de diálogo descrito por esta tabla para mostrar tiene dos controles: una etiqueta y un control de edición. La **estructura DTBLLBX** tiene un miembro de desplazamiento de etiqueta, al igual que varias de las estructuras de control, que describe dónde comienza la cadena de caracteres de la etiqueta. Las cadenas de caracteres de etiqueta normalmente se colocan en la memoria inmediatamente después de la estructura. 
  
**Visualización de las estructuras de la tabla**
  
![Mostrar estructuras de tabla](media/dtstruct.gif "Mostrar estructuras de tabla")
  
## <a name="see-also"></a>Vea también

- [Implementación de la tabla para mostrar](display-table-implementation.md)

