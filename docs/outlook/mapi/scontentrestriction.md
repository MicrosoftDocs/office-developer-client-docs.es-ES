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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 34177aee48adad7eecb40836a247705fc22d2a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820594"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**Se aplica a**: Outlook 
  
Describe una restricción de contenido, que se usa para limitar una vista de tabla a sólo las filas en las que incluyen una columna con contenido que coinciden con una cadena de búsqueda. 
  
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
  
> Configuración de opción definir el nivel de precisión que se debe aplicar la restricción de contenido al comprobar una coincidencia.
    
   Los **16 bits inferiores** del miembro **ulFuzzyLevel** se aplican a las propiedades de tipo PT_BINARY y PT_STRING8 y debe establecerse en uno de los siguientes valores: 
    
   - FL_FULLSTRING: Para hacer coincidir, la cadena de búsqueda **lpProp** debe estar incluida en la propiedad identificada por **ulPropTag**.
        
   - FL_PREFIX: Para hacer coincidir, la cadena de búsqueda **lpProp** debe aparecer al principio de la propiedad identificada por **ulPropTag**. Las dos cadenas deben compararse sólo hasta la longitud de la cadena de búsqueda indicada por **lpProp**. 
        
   - FL_SUBSTRING: Para hacer coincidir, la cadena de búsqueda **lpProp** debe estar incluida en cualquier lugar en la propiedad identificada por **ulPropTag**. 
        
   Los **16 bits superiores** del miembro **ulFuzzyLevel** sólo se aplican a las propiedades de tipo PT_STRING8 y se puede establecer en los siguientes valores en cualquier combinación: 
        
   - FL_IGNORECASE: La comparación debe realizarse sin tener en cuenta el caso. 
        
   - FL_IGNORENONSPACE: La comparación debe omitir definidas en Unicode caracteres sin espacios, como los signos diacríticos. 
        
   - FL_LOOSE: La comparación debería proporcionarle a una coincidencia siempre que sea posible, se omite caso y caracteres sin espacios. 
    
**ulPropTag**
  
> Etiqueta de la propiedad que identifica la propiedad de cadena para buscar la aparición de la cadena de búsqueda. 
    
**lpProp**
  
> Puntero a una estructura de valor de propiedad que contiene el valor de cadena que se utilizará como la cadena de búsqueda.
    
## <a name="remarks"></a>Notas

Hay dos etiquetas de propiedad en una estructura de **SContentRestriction** : uno en el miembro **ulPropTag** y la otra en el miembro **ulPropTag** de la estructura **SPropValue** apunta a **lpProp**. En ambas etiquetas, MAPI requiere sólo el campo de tipo de propiedad y omite el campo de identificador de la propiedad. Sin embargo, deben coincidir con los tipos de dos propiedades, o bien el valor de error MAPI_E_TOO_COMPLEX se devuelve cuando se utiliza la restricción de una llamada a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md). 
  
Los valores FL_FULLSTRING, FL_PREFIX y FL_SUBSTRING son mutuamente excluyentes. Se puede establecer sólo uno de ellos y uno de ellos se debe establecer. Se corrigen sus significados, y debe implementar el proveedor exactamente como se definió. El proveedor debe devolver MAPI_E_TOO_COMPLEX si no es capaz de admitir estos valores. 
  
Los valores FL_IGNORECASE, FL_IGNORENONSPACE y FL_LOOSE son independientes. En cualquier lugar de cero a las tres de ellos se puede establecer. Sus definiciones se proporcionan sólo como orientación, y el proveedor es libre de implementar su propio significado específico de cada indicador. El proveedor no debe devolver cualquier indicación de error si no tiene implementación de un indicador especificado. 
  
El resultado de una restricción de contenido impuesta con respecto a una propiedad no está definido cuando la propiedad no existe. Cuando un cliente requiere un comportamiento bien definido para esta restricción y no está seguro de si la propiedad existe por ejemplo, no es una columna de una tabla necesaria debe crear una restricción **y** para unirse a la restricción de contenido con una restricción existe. Usar una estructura [SExistRestriction](sexistrestriction.md) para definir la restricción existe y una estructura [SAndRestriction](sandrestriction.md) para definir la restricción de **y** . 
  
Para obtener más información sobre la estructura de **SContentRestriction** y restricciones en general, vea [Acerca de las restricciones](about-restrictions.md).
  
## <a name="see-also"></a>Ver también

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [Estructuras MAPI](mapi-structures.md)

