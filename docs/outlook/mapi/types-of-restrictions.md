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
  
Hay muchos tipos de restricciones, algunas que se centran en columnas específicas. Se espera que todas las implementaciones de tabla admitan restricciones en las columnas del conjunto de columnas actual. Sin embargo, para agregar valor, los implementadores de tablas también pueden admitir restricciones basadas en propiedades de objeto que no están actualmente en la vista de tabla.
  
Algunas restricciones se pueden combinar mediante una restricción que realiza una operación **lógica AND**, **OR** o **NOT.** Por ejemplo, la mayoría de las restricciones de propiedad deben unirse a las restricciones existentes mediante **restricciones AND.** Hay algunas excepciones, como cuando la propiedad usada en la restricción de propiedad es la propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) o cuando es una columna necesaria en una tabla. Las restricciones de creación de cliente para limitar su vista deben usar restricciones existentes con sus restricciones de propiedad porque MAPI no especifica cómo deben evaluarse los proveedores de servicios las restricciones de propiedades cuando no existe una propiedad. Es razonable y recomendado que los proveedores de servicios fallen la restricción, pero no hay requisitos. 
  
Una restricción se define mediante la estructura de datos [de SRestriction](srestriction.md) que contiene una unión de estructuras de restricción más especializadas y un indicador del tipo de estructura incluida en la unión. 
  
Cada una de las estructuras de restricción especializadas de la unión representa un tipo diferente de restricción. Los tipos de restricciones y sus estructuras de datos asociadas son:
  
|**Tipo de restricción**|**Estructura de datos asociada**|**Descripción**|
|:-----|:-----|:-----|
|Compare (propiedad)  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Compara dos propiedades del mismo tipo.  <br/> |
|**Y** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Realiza una operación **AND lógica** con dos o más restricciones.  <br/> |
|**OR** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Realiza una operación **OR lógica** en dos o más restricciones.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Realiza una operación **LÓGICA NOT** en dos o más restricciones.  <br/> |
|Contenido  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Localiza los datos especificados.  <br/> |
|Propiedad  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Especifica un valor de propiedad determinado como criterios para la coincidencia. Se puede usar, por ejemplo, para buscar un tipo determinado de datos adjuntos.  <br/> |
|Bitmask  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Aplica una máscara de bits a una PT_LONG propiedad, normalmente para determinar si se establecen marcas concretas.  <br/> |
|Size  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Comprueba el tamaño de una propiedad con operadores relacionales estándar.  <br/> |
|Existir  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Comprueba si un objeto tiene un valor para una propiedad.  <br/> |
|Subobjeto  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Se usa para buscar a través de subobjetos u objetos a los que no se puede tener acceso con un identificador de entrada, como destinatarios y datos adjuntos. Se puede usar, por ejemplo, para buscar mensajes para un destinatario determinado.  <br/> |
|Comentario  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Asocia un objeto con un conjunto de propiedades con nombre.  <br/> |
   
Algunas restricciones usan expresiones regulares y MAPI admite una forma limitada de la notación de expresiones regulares en el estilo que se usa en muchas aplicaciones de texto.
  
Los clientes que guardan restricciones en el disco usan la restricción de comentarios para mantener la información específica de la aplicación con la restricción. Por ejemplo, un cliente que guarda el nombre de una propiedad con nombre usada en una restricción de propiedad puede hacerlo con una restricción de comentario. No es posible guardar el nombre en una restricción de propiedad; la [estructura de datos SPropertyRestriction](spropertyrestriction.md) solo contiene la etiqueta de propiedad. [IMAPITable::Restrict](imapitable-restrict.md) omite las restricciones de comentarios porque no tienen ningún efecto en las filas  devueltas por [IMAPITable::QueryRows](imapitable-queryrows.md) después de realizar una llamada restrict. 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

