---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406090"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción de propiedad que se usa para coincidir con una constante con el valor de una propiedad.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a>Members

**relop**
  
> Operador relacional que se usará en la búsqueda. Los valores posibles son los siguientes:
    
  - RELOP_GE: la comparación se realiza en función de un primer valor mayor o igual.
        
  - RELOP_GT: la comparación se realiza en función de un primer valor mayor.
        
  - RELOP_LE: la comparación se realiza en función de un primer valor menor o igual.
        
  - RELOP_LT: la comparación se realiza en función de un primer valor menor.
        
  - RELOP_NE: la comparación se realiza en función de valores desiguales.
        
  - RELOP_RE: la comparación se realiza en función de los valores LIKE (expresión regular).
        
  - RELOP_EQ: la comparación se realiza en función de valores iguales.
    
**ulPropTag**
  
> Etiqueta de propiedad que identifica la propiedad que se va a comparar. 
    
**lpProp**
  
> Puntero a una [estructura SPropValue](spropvalue.md) que contiene el valor de constante que se usará en la comparación. 
    
## <a name="remarks"></a>Comentarios

Hay dos etiquetas de propiedad en una **estructura SPropertyRestriction.** Uno está en el **miembro ulPropTag** y el otro está en el **miembro ulPropTag** de la estructura **SPropValue** apuntada por **lpProp**. MAPI requiere el campo identificador de propiedad y el campo de tipo de propiedad. El **ulPropTag** de **SPropertyRestriction** es la propiedad que se va a coincidir y el puntero **lpProp** de **SPropertyRestriction** al tipo **ulPropTag**'s del **SPropValue** indica cómo se interpretan el valor de los miembros de la unión **lpProp.** Los dos tipos de propiedad deben coincidir o, de lo contrario, el valor de error MAPI_E_TOO_COMPLEX se devuelve cuando se usa la restricción en una llamada a [IMAPITable::Restrict](imapitable-restrict.md) o [IMAPITable::FindRow](imapitable-findrow.md). 
  
El orden de comparación es _(valor de propiedad) (operador relacional) (valor constante)._
  
Cuando se pasa una restricción de propiedad a **IMAPITable::Restrict** o **IMAPITable::FindRow** y la propiedad de destino no existe, los resultados de la restricción no están definidos. Al crear una **restricción AND** que une la restricción de propiedad con una restricción **EXIST,** se puede garantizar a un autor de la llamada resultados precisos. Use una [estructura SExistRestriction](sexistrestriction.md) para definir la restricción **EXIST** y una estructura [SAndRestriction](sandrestriction.md) para definir la **restricción AND.** 
  
Las etiquetas de propiedades de varios valores se pueden usar en restricciones de propiedad si el proveedor de servicios que implementa la tabla las admite. Si se admite, las etiquetas de propiedades multivalor se pueden usar en cualquier lugar donde se puedan usar etiquetas de propiedad de un solo valor. 
  
Las etiquetas de propiedades de varios valores se pueden usar en los siguientes métodos:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Un caso notable cuando las dos etiquetas de propiedad no coinciden es si se restringe en una propiedad de varios valores. En este caso, lo siguiente debe ser true. > Si el tipo de propiedad **del ulPropTag** de **SPropertyRestriction** contiene la marca de bits de tipo de propiedad multivalor MV_FLAG (0x1000), el tipo de propiedad **del ulPropTag** de **SPropValue** debe coincidir con el primero menos la marca de bits MV_FLAG, es decir, su inversa. > Por ejemplo, para restringir el uso de una propiedad de cadena personalizada de varios valores, como una categoría con una etiqueta de propiedad para la propiedad 0x8012101f, es decir, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), la **SPropertyRestriction** correspondiente aparecería de la siguiente manera. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> tenga en cuenta que si el tipo de propiedad **de ulPropTag** de **SPropValue** contiene la marca de bits MV_FLAG, es probable que se devuelva MAPI_E_TOO_COMPLEX. 
  
Para obtener más información acerca **de la estructura SPropertyRestriction,** vea [About Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Vea también

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [Estructuras MAPI](mapi-structures.md)

