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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339840"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción de contenido, que se usa para limitar una vista de tabla a sólo las filas que incluyen una columna con el contenido que coincide con una cadena de búsqueda. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a>Members

**ulFuzzyLevel**
  
> Opciones que definen el nivel de precisión que debe cumplir la restricción de contenido cuando se comprueba si coinciden.
    
   Los **16 bits inferiores** del miembro **ulFuzzyLevel** se aplican a las propiedades del tipo PT_BINARY y PT_STRING8 y deben establecerse en uno de los valores siguientes: 
    
   - FL_FULLSTRING: para que se cumpla, la cadena de búsqueda **lpProp** debe estar contenida en la propiedad identificada por **ulPropTag**.
        
   - FL_PREFIX: para que se cumpla, la cadena de búsqueda **lpProp** debe aparecer al principio de la propiedad identificada por **ulPropTag**. Las dos cadenas solo deben compararse hasta la longitud de la cadena de búsqueda indicada por **lpProp**. 
        
   - FL_SUBSTRING: para que se cumpla, la cadena de búsqueda **lpProp** debe estar contenida en cualquier parte de la propiedad identificada por **ulPropTag**. 
        
   Los **16 bits superiores** del miembro **ulFuzzyLevel** solo se aplican a propiedades de tipo PT_STRING8 y se pueden establecer en cualquier combinación de los siguientes valores: 
        
   - FL_IGNORECASE: la comparación debe realizarse sin tener en cuenta el caso. 
        
   - FL_IGNORENONSPACE: la comparación debe omitir los caracteres no de espaciado definidos en Unicode, como las marcas diacríticas. 
        
   - FL_LOOSE: la comparación debe darle una coincidencia siempre que sea posible, sin tener en cuenta los caracteres de mayúsculas y minúsculas. 
    
**ulPropTag**
  
> Etiqueta de propiedad que identifica la propiedad de cadena que se va a comprobar para comprobar si se ha encontrado la cadena de búsqueda. 
    
**lpProp**
  
> Puntero a una estructura de valor de propiedad que contiene el valor de cadena que se va a usar como cadena de búsqueda.
    
## <a name="remarks"></a>Comentarios

Hay dos etiquetas de propiedad en una estructura **SContentRestriction** : una en el miembro **ulPropTag** y otra en el miembro **ulPropTag** de la estructura **SPropValue** a la que apunta **lpProp**. En ambas etiquetas, MAPI solo requiere el campo de tipo de propiedad y omite el campo de identificador de propiedad. Sin embargo, los dos tipos de propiedad deben coincidir o, de lo contrario, se devuelve el valor de error MAPI_E_TOO_COMPLEX cuando se usa la restricción en una llamada a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md). 
  
Los valores FL_FULLSTRING, FL_PREFIX y FL_SUBSTRING se excluyen mutuamente. Solo se puede establecer una de ellas y se debe establecer una de ellas. Los significados son fijos y el proveedor debe implementarlos exactamente como están definidos. El proveedor debe devolver MAPI_E_TOO_COMPLEX si no puede admitir estos valores. 
  
Los valores FL_IGNORECASE, FL_IGNORENONSPACE y FL_LOOSE son independientes. Se puede establecer cualquier parte de cero a los tres. Sus definiciones se proporcionan solo como guía y el proveedor es gratuito para implementar su propio significado específico de cada marca. El proveedor no debe devolver ninguna indicación de error si no tiene ninguna implementación de un indicador especificado. 
  
El resultado de una restricción de contenido impuesta a una propiedad no está definido cuando la propiedad no existe. Cuando un cliente requiere un comportamiento bien definido para dicha restricción y no está seguro de si la propiedad existe por ejemplo, no es una columna obligatoria de una tabla, por lo que debe crear una restricción **and** para unirse a la restricción de contenido con una restricción exist. Use una estructura [SExistRestriction](sexistrestriction.md) para definir la restricción EXISTS y una estructura [SAndRestriction](sandrestriction.md) para definir la restricción **and** . 
  
Para obtener más información acerca de las restricciones y la estructura **SContentRestriction** en general, consulte [About Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Vea también

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [Estructuras MAPI](mapi-structures.md)

