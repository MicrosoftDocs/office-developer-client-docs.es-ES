---
title: Tipos de restricciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 85cf254c9ea23ecbd6f311ba012d2e048a0b2a6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572448"
---
# <a name="types-of-restrictions"></a>Tipos de restricciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Existen muchos tipos de restricciones, algunos que se centran en columnas específicas. Se esperan que todas las implementaciones de tabla admite restricciones en las columnas en el conjunto actual de la columna. Sin embargo, para agregar valor, implementadores de tabla también pueden admitir restricciones en función de las propiedades del objeto que no están actualmente en la vista de tabla.
  
Algunas restricciones se pueden combinar con una restricción que realiza una operación lógica **AND**, **u**o **no** . Por ejemplo, la propiedad mayoría restricciones deben estar unidas con existe restricciones de uso **y** restricciones. Hay algunas excepciones, como cuando la propiedad que se usa en la restricción de propiedad es la propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) o cuando es una columna necesaria en una tabla. Un cliente de creación de restricciones para limitar su vista debería haber restricciones con sus restricciones de propiedad uso porque MAPI no especifica cómo los proveedores de servicios deben evaluar las restricciones de propiedad cuando una propiedad no existe. Es razonable y se recomienda que los proveedores de servicios producirá un error en la restricción, pero no existen requisitos. 
  
Una restricción se define mediante la estructura de datos [SRestriction](srestriction.md) que contiene una unión de las estructuras de restricción más especializadas y un indicador del tipo de estructura que se incluyen en la unión. 
  
Cada una de las estructuras de restricción especializados en la unión representa un tipo diferente de restricción. Los tipos de restricciones y sus estructuras de datos asociados son:
  
|**Tipo de restricción**|**Estructura de datos asociada**|**Descripción**|
|:-----|:-----|:-----|
|Comparar (propiedad)  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Compara dos propiedades del mismo tipo.  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Realiza una operación **AND** lógica en dos o más restricciones.  <br/> |
|**O** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Realiza una operación **OR** lógica en dos o más restricciones.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Realiza una operación **NOT** lógica en dos o más restricciones.  <br/> |
|Content  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Busca datos especificado.  <br/> |
|Propiedad  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Especifica un valor de esa propiedad como criterios de coincidencia. Puede utilizarse, por ejemplo, para buscar un determinado tipo de datos adjuntos.  <br/> |
|Bitmask  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Se aplica una máscara de bits para una propiedad PT_LONG, normalmente para determinar si se establecen indicadores determinados.  <br/> |
|Size  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Comprueba el tamaño de una propiedad mediante operadores relacionales estándar.  <br/> |
|Existe  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Comprueba si un objeto tiene un valor para una propiedad.  <br/> |
|Subobjetos  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Se usa para buscar a través de subobjetos u objetos que no se pueden tener acceso con un identificador de entrada, como los destinatarios y los datos adjuntos. Puede utilizarse, por ejemplo, para buscar los mensajes de un destinatario concreto.  <br/> |
|Comment  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Asocia un objeto a un conjunto de propiedades con nombre.  <br/> |
   
Algunas restricciones usan expresiones regulares y MAPI admite una forma limitada de expresión regular notación en el estilo que usa muchas aplicaciones de texto.
  
La restricción de comentario se usa en los clientes que guardar restricciones en disco para mantener la información específica de la aplicación con la restricción. Por ejemplo, un cliente de guardar el nombre de una propiedad con nombre que se usa en una restricción de propiedad puede hacerlo con una restricción de comentario. Guardar el nombre no es posible en una restricción de propiedad; la estructura de datos [SPropertyRestriction](spropertyrestriction.md) contiene sólo la etiqueta de propiedad. Restricciones de comentario se omiten por [IMAPITable:: Restrict](imapitable-restrict.md) en que no tienen ningún efecto en las filas devueltas por [IMAPITable:: QueryRows](imapitable-queryrows.md) después de que se ha realizado una llamada **Restrict** . 
  
## <a name="see-also"></a>Recursos adicionales



[Tablas MAPI](mapi-tables.md)

