---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423667"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción de contenido, que se usa para limitar una vista de tabla solo a aquellas filas que incluyen una columna con contenido que coincide con una cadena de búsqueda. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a>Miembros

**ulFuzzyLevel**
  
> Configuración de opciones que define el nivel de precisión que debe aplicar la restricción de contenido al comprobar si hay una coincidencia.
    
   Los **16 bits** inferiores del miembro **ulFuzzyLevel** se aplican a las propiedades del tipo PT_BINARY y PT_STRING8 y deben establecerse en uno de los siguientes valores: 
    
   - FL_FULLSTRING: Para que coincida, la cadena de búsqueda **lpProp** debe estar incluida en la propiedad identificada por **ulPropTag**.
        
   - FL_PREFIX : Para que coincida, la cadena de búsqueda **lpProp** debe aparecer al principio de la propiedad identificada por **ulPropTag**. Las dos cadenas deben compararse solo hasta la longitud de la cadena de búsqueda indicada por **lpProp**. 
        
   - FL_SUBSTRING: Para que coincida, la cadena de búsqueda **lpProp** debe estar contenida en cualquier parte de la propiedad identificada por **ulPropTag**. 
        
   Los **16 bits** superiores del miembro **ulFuzzyLevel** solo se aplican a las propiedades de tipo PT_STRING8 y se pueden establecer en los siguientes valores en cualquier combinación: 
        
   - FL_IGNORECASE: la comparación debe realizarse sin tener en cuenta las mayúsculas y minúsculas. 
        
   - FL_IGNORENONSPACE: la comparación debe omitir los caracteres no espaciado definidos por Unicode, como los signos diacríticos. 
        
   - FL_LOOSE: la comparación debe proporcionar una coincidencia siempre que sea posible, ignorando los caracteres de mayúsculas y minúsculas y sin espaciado. 
    
**ulPropTag**
  
> Etiqueta de propiedad que identifica la propiedad de cadena que se va a comprobar para la aparición de la cadena de búsqueda. 
    
**lpProp**
  
> Puntero a una estructura de valores de propiedad que contiene el valor de cadena que se usará como cadena de búsqueda.
    
## <a name="remarks"></a>Comentarios

Hay dos etiquetas de propiedad en una estructura **SContentRestriction:** una en el miembro **ulPropTag** y la otra en el **miembro ulPropTag** de la estructura **SPropValue** apuntada por **lpProp**. En ambas etiquetas, MAPI solo requiere el campo de tipo de propiedad y omite el campo de identificador de propiedad. Sin embargo, los dos tipos de propiedad deben coincidir o, de lo contrario, se devuelve el valor de error MAPI_E_TOO_COMPLEX cuando se usa la restricción en una llamada a [IMAPITable::Restrict](imapitable-restrict.md) o [IMAPITable::FindRow](imapitable-findrow.md). 
  
Los valores FL_FULLSTRING, FL_PREFIX y FL_SUBSTRING son mutuamente excluyentes. Solo se puede establecer uno de ellos y uno de ellos debe establecerse. Sus significados son fijos y el proveedor debe implementarlos exactamente según lo definido. El proveedor debe devolver MAPI_E_TOO_COMPLEX si no puede admitir estos valores. 
  
Los valores FL_IGNORECASE, FL_IGNORENONSPACE y FL_LOOSE son independientes. Se pueden establecer en cualquier lugar desde cero hasta los tres. Sus definiciones solo se proporcionan como instrucciones y el proveedor puede implementar su propio significado específico de cada marca. El proveedor no debe devolver ninguna indicación de error si no tiene ninguna implementación de una marca especificada. 
  
El resultado de una restricción de contenido impuesta a una propiedad es indefinido cuando la propiedad no existe. Cuando un cliente requiere un comportamiento bien definido para dicha restricción y no está seguro de si la propiedad existe, por ejemplo, no es una columna necesaria de una tabla, debe crear una restricción **AND** para unir la restricción de contenido con una restricción existente. Use una [estructura SExistRestriction](sexistrestriction.md) para definir la restricción existente y una estructura [SAndRestriction](sandrestriction.md) para definir la **restricción AND.** 
  
Para obtener más información acerca **de la estructura SContentRestriction** y las restricciones en general, vea [Acerca de las restricciones](about-restrictions.md).
  
## <a name="see-also"></a>Consulte también

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [Estructuras MAPI](mapi-structures.md)

