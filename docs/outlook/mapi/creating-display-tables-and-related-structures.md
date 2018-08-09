---
title: Creación de tablas para mostrar y estructuras relacionadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 177fe21537e921a4b94a34ad531847701b16c344
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816612"
---
# <a name="creating-display-tables-and-related-structures"></a>Creación de tablas para mostrar y estructuras relacionadas
  
**Hace referencia a**: Outlook 
  
Creación de una tabla para mostrar es similar a escribir un programa con un lenguaje de scripting. Puede crear una tabla para mostrar por una llamada a [BuildDisplayTable](builddisplaytable.md) o escribir código personalizado para rellenar las filas y columnas de la tabla. En general, debe utilizar la técnica **BuildDisplayTable** porque es más sencilla. 
  
Para poder llamar **BuildDisplayTable** para que solicite MAPI para crear una tabla para mostrar, hay una jerarquía de estructuras que se deben generar. La estructura de nivel superior, [DTPAGE](dtpage.md), describe una página de propiedades con fichas único. En cada **DTPAGE** estructura es una estructura [DTCTL](dtctl.md) que describe un control único, como un cuadro de edición o un botón de opción. Cada estructura **DTCTL** contiene una estructura que es específica para el tipo de control. Por ejemplo, si la estructura **DTCTL** describe un control de cuadro de edición, contendrá una estructura **DTBLEDIT** . La estructura **DTCTL** para un botón de opción contiene una estructura **DTBLRADIOBUTTON** . 
  
Estas estructuras directamente relacionados con la **BuildDisplayTable**; no tienen ningún significado fuera del contexto de esta función. Cuando se llama a **BuildDisplayTable**, pase una o más estructuras **DTPAGE** como parámetros de entrada. Las estructuras **DTPAGE** contienen una matriz de estructuras **DTCTL** y un recuento del número de estructuras **DTCTL** en la matriz. Hay una estructura para cada control que se muestra en el cuadro de diálogo. Las estructuras **DTPAGE** también tienen una cadena de caracteres que representa el nombre de una ayuda de archivo y cuadro de diálogo cuadro recurso correspondiente. 
  
Cada estructura **DTCTL** en una estructura **DTPAGE** contiene los siguientes datos que se usan para establecer las propiedades para el control: 
  
- El tipo de control para la configuración de **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)).
    
- Indicadores de control para la configuración de **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
    
- Datos de notificación para la configuración de **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)).
    
- La estructura de control para la configuración de **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).
    
Estructuras **DTCTL** también contienen un identificador de recursos y, para editar y controles de cuadro combinado, un filtro de carácter. 
  
El miembro de la estructura de control de una estructura **DTCTL** describe los datos que sea únicos para el tipo de control. MAPI define una estructura diferente para cada tipo de control. Por ejemplo, los datos de un control de edición se representan mediante una estructura **DTBLEDIT** ; los datos de un cuadro de lista está representados por una estructura **DTBLLBX** . 
  
En la siguiente ilustración, se muestra la relación entre los tres tipos de estructuras de tabla para mostrar. Se describe en esta tabla para mostrar el cuadro de diálogo tiene dos controles: una etiqueta y un control de edición. La estructura **DTBLLBX** tiene un miembro de desplazamiento de etiqueta, como realizar algunas de las estructuras de control, que se describe dónde comienza la cadena de caracteres para la etiqueta. Las cadenas de caracteres de etiqueta normalmente se colocan en la memoria que sigue inmediatamente a la estructura. 
  
**Visualización de las estructuras de la tabla**
  
![Estructuras de tabla para mostrar] (media/dtstruct.gif "Estructuras de tabla para mostrar")
  
## <a name="see-also"></a>Vea también

- [Implementación de la tabla para mostrar](display-table-implementation.md)

