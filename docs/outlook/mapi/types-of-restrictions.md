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
ms.openlocfilehash: 28159dfb947b4fb0ea54680627588b7c10bee3b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416289"
---
# <a name="types-of-restrictions"></a>Tipos de restricciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay muchos tipos de restricciones, algunas que se centran en columnas específicas. Se espera que todas las implementaciones de tabla admitan restricciones en las columnas del conjunto de columnas actual. Sin embargo, para agregar valor, los implementadores de tabla también pueden admitir restricciones basadas en propiedades de objeto que no se encuentran actualmente en la vista de tabla.
  
Algunas restricciones se pueden combinar mediante una restricción que realiza una operación lógica **and**, **or**o **Not** . Por ejemplo, la mayoría de las restricciones de propiedad deben combinarse con restricciones EXISTS con restricciones **y** . Hay algunas excepciones, como cuando la propiedad usada en la restricción de propiedad es la propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) o cuando es una columna obligatoria de una tabla. Una restricción de la creación de clientes para limitar su vista debe usar restricciones existentes con sus restricciones de propiedad, ya que MAPI no especifica cómo los proveedores de servicios deben evaluar las restricciones de propiedad cuando una propiedad no existe. Es razonable y se recomienda que los proveedores de servicios den error en la restricción, pero no hay requisitos. 
  
Una restricción se define mediante la estructura de datos [SRestriction](srestriction.md) , que contiene una Unión de estructuras de restricción más especializadas y un indicador del tipo de estructura incluida en la Unión. 
  
Cada una de las estructuras de restricción especializadas de la Unión representa un tipo de restricción diferente. Los tipos de restricciones y las estructuras de datos asociadas son los siguientes:
  
|**Tipo de restricción**|**Estructura de datos asociada**|**Descripción**|
|:-----|:-----|:-----|
|Compare (propiedad)  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Compara dos propiedades del mismo tipo.  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Realiza una operación lógica **and** en dos o más restricciones.  <br/> |
|**O** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Realiza una operación **or** lógica en dos o más restricciones.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Realiza una operación **Not** lógica en dos o más restricciones.  <br/> |
|Contenido  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Busca datos especificados.  <br/> |
|Propiedad  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Especifica un valor de propiedad concreto como criterio para la coincidencia. Puede usarse, por ejemplo, para buscar un tipo concreto de datos adjuntos.  <br/> |
|Máscara  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Aplica una máscara de PT_LONG a una propiedad de, normalmente para determinar si se han establecido determinados marcadores.  <br/> |
|Size  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Comprueba el tamaño de una propiedad mediante operadores relacionales estándar.  <br/> |
|Haber  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Comprueba si un objeto tiene un valor para una propiedad.  <br/> |
|Subobjeto  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Se usa para buscar en los subobjetos o los objetos a los que no se puede tener acceso con un identificador de entrada, como los destinatarios y los datos adjuntos. Puede usarse, por ejemplo, para buscar mensajes de un destinatario en particular.  <br/> |
|Comentario  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Asocia un objeto a un conjunto de propiedades con nombre.  <br/> |
   
Algunas restricciones usan expresiones regulares y MAPI admite una forma limitada de la notación de expresiones regulares en el estilo que usa muchas aplicaciones de texto.
  
La restricción de comentarios es usada por los clientes que guardan restricciones en el disco para mantener la información específica de la aplicación con la restricción. Por ejemplo, un cliente que guarda el nombre de una propiedad con nombre que se usa en una restricción de propiedad puede hacerlo con una restricción de comentario. No es posible guardar el nombre en una restricción de propiedad; la estructura de datos [SPropertyRestriction](spropertyrestriction.md) contiene solo la etiqueta Property. El método de restricción de comentarios es ignorado por [IMAPITable:: Restrict](imapitable-restrict.md) en el sentido de que no tienen ningún efecto sobre las filas devueltas por el [IMAPITable:: QueryRows](imapitable-queryrows.md) después de realizar una llamada a **Restrict** . 
  
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

