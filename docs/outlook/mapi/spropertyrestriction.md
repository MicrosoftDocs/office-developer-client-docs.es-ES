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
ms.openlocfilehash: f59b0041f271010e56dda2f73d2248f133bc1325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820732"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**Hace referencia a**: Outlook 
  
Describe una restricción de propiedad que se usa para que coincida con una constante con el valor de una propiedad.
  
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

**RelOp**
  
> Operador relacional que se usará en la búsqueda. Los valores posibles son los siguientes:
    
  - RELOP_GE: Se realiza la comparación basándose en el primer valor mayor o igual.
        
  - RELOP_GT: Se realiza la comparación basándose en un valor mayor de primera.
        
  - RELOP_LE: Se realiza la comparación basándose en el primer valor menor o igual.
        
  - RELOP_LT: Se realiza la comparación basándose en un valor menor de primera.
        
  - RELOP_NE: Se realiza la comparación basándose en valores desiguales.
        
  - RELOP_RE: La comparación se realiza en función de como valores (expresión regular).
        
  - RELOP_EQ: Se realiza la comparación basándose en valores iguales.
    
**ulPropTag**
  
> Etiqueta de la propiedad que identifica la propiedad que se va a comparar. 
    
**lpProp**
  
> Puntero a una estructura [SPropValue](spropvalue.md) que contiene el valor constante que se utilizará en la comparación. 
    
## <a name="remarks"></a>Comentarios

Hay dos etiquetas de propiedad en una estructura **SPropertyRestriction** . Uno se encuentra en el miembro **ulPropTag** y la otra es en el miembro **ulPropTag** de la estructura **SPropValue** que señala **lpProp**. MAPI requiere el campo de identificador de la propiedad y el campo de tipo de propiedad. El **ulPropTag** en **SPropertyRestriction** es la propiedad que coincida, y el puntero de **lpProp** de la **SPropertyRestriction** a la **ulPropTag**del tipo de la **SPropValue** indica cómo el valor de los miembros de la Unión de **lpProp** se interpretan. Deben coincidir con los tipos de dos propiedades, o bien el valor de error MAPI_E_TOO_COMPLEX se devuelve cuando se utiliza la restricción de una llamada a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md). 
  
El orden de comparación es _(valor de la propiedad) (operador relacional) (valor constante)_.
  
Cuando una restricción de propiedad se pasa al **IMAPITable:: Restrict** o **IMAPITable:: FindRow** y la propiedad de destino no existe, no están definidos los resultados de la restricción. Mediante la creación de una restricción **y** que se une a la restricción de propiedad con una restricción **existe** , un autor de la llamada se pueda garantizar resultados precisos. Usar una estructura [SExistRestriction](sexistrestriction.md) para definir la restricción **existe** y una estructura [SAndRestriction](sandrestriction.md) para definir la restricción de **y** . 
  
Etiquetas de varios valores de propiedad se pueden usar en restricciones de propiedad si el proveedor de servicios de implementación de la tabla es compatible con ellos. Si se admite, se pueden usar etiquetas de varios valores de propiedad en cualquier lugar se pueden usar las etiquetas de propiedad de un solo valor. 
  
Etiquetas de propiedad de varios valores se pueden usar en los siguientes métodos:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Un caso notable cuando no coinciden con las etiquetas de dos propiedades es si restricción en una propiedad de varios valor. En este caso lo siguiente debe ser true. > Si el tipo de propiedad de la **ulPropTag** de **SPropertyRestriction** contiene el indicador de bits de tipo de propiedad de valor múltiple MV_FLAG (0 x 1000), el tipo de propiedad de la **ulPropTag** de **SPropValue** debe coincidir con la primera menos el MV_ Indicador de bits de indicador, es decir, su inversa. > Por ejemplo, para restringir el uso de una propiedad de cadena personalizada de varios valores, como una categoría con una etiqueta de propiedad para la propiedad 0x8012101f, es decir, PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012)), el correspondiente **SPropertyRestriction** aparecería como se muestra a continuación. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Tenga en cuenta que si el tipo de propiedad de la **ulPropTag** de **SPropValue** contiene el indicador de bits MV_FLAG, la devolución probablemente es MAPI_E_TOO_COMPLEX. 
  
Para obtener más información acerca de la estructura **SPropertyRestriction** , vea [Acerca de las restricciones](about-restrictions.md). 
  
## <a name="see-also"></a>Vea también

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [Estructuras MAPI](mapi-structures.md)

