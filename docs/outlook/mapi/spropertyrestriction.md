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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357858"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una restricción de propiedad que se usa para hacer coincidir una constante con el valor de una propiedad.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Operador relacional que se utilizará en la búsqueda. Los valores posibles son los siguientes:
    
  - RELOP_GE: la comparación se realiza en función de un valor mayor o igual al primero.
        
  - RELOP_GT: la comparación se realiza en función de un primer valor superior.
        
  - RELOP_LE: la comparación se realiza en función de un valor menor o igual al primero.
        
  - RELOP_LT: la comparación se realiza en función de un valor primero menor.
        
  - RELOP_NE: la comparación se realiza en función de valores desiguales.
        
  - RELOP_RE: la comparación se realiza en función de los valores LIKE (expresión regular).
        
  - RELOP_EQ: la comparación se realiza en función de los valores iguales.
    
**ulPropTag**
  
> Etiqueta de propiedad que identifica la propiedad que se va a comparar. 
    
**lpProp**
  
> Puntero a una estructura [SPropValue](spropvalue.md) que contiene el valor constante que se usará en la comparación. 
    
## <a name="remarks"></a>Comentarios

Hay dos etiquetas de propiedad en una estructura **SPropertyRestriction** . Uno está en el miembro **ulPropTag** y el otro en el miembro **ulPropTag** de la estructura **SPropValue** a la que apunta **lpProp**. MAPI requiere el campo de identificador de propiedad y el campo de tipo de propiedad. **UlPropTag** en **SPropertyRestriction** es la propiedad que se va a comparar y el puntero **lpProp** del **SPropertyRestriction** al tipo de **ulPropTag**de la **SPropValue** indica cómo el valor de los miembros del se interpreta **lpProp** Union. Los dos tipos de propiedad deben coincidir o, de lo contrario, se devuelve el valor de error MAPI_E_TOO_COMPLEX cuando se usa la restricción en una llamada a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md). 
  
El orden de comparación es _(valor de propiedad) (operador relacional) (valor constante)_.
  
Cuando se pasa una restricción de propiedad a **IMAPITable:: Restrict** o **IMAPITable:: FindRow** y la propiedad de destino no existe, los resultados de la restricción quedan sin definir. Mediante la creación de una restricción **and** que combina la restricción de propiedad con una restricción **exist** , una persona que llama puede garantizar resultados precisos. Use una estructura [SExistRestriction](sexistrestriction.md) para definir la restricción **EXISTS** y una estructura [SAndRestriction](sandrestriction.md) para definir la restricción **and** . 
  
Las etiquetas de propiedad con varios valores se pueden usar en las restricciones de propiedad si el proveedor de servicios que implementa la tabla las admite. Si se admite, se pueden usar etiquetas de propiedad de varios valores en cualquier lugar donde se puedan usar etiquetas de propiedad de un solo valor. 
  
Las etiquetas de propiedad con varios valores se pueden usar en los métodos siguientes:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Un caso notable en el que las dos etiquetas de propiedad no coincidirán es si se limita a una propiedad de varios valores. En este caso, debe cumplirse lo siguiente. > si el tipo de propiedad del **ulPropTag** de **SPropertyRestriction** contiene el marcador de bits de tipo de propiedad de varios valores MV_FLAG (0x1000), el tipo de propiedad del **ulPropTag** de **SPropValue** debe coincidir con el primero menos el MV_ Marcar el indicador de bits, es decir, su inverso. > por ejemplo, para restringir el uso de una propiedad de cadena personalizada de varios valores como una categoría con una etiqueta de propiedad para la propiedad 0x8012101f, es decir, PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012)), el **SPropertyRestriction** correspondiente aparecerá como después. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> tenga en cuenta que si el tipo de propiedad del **ulPropTag** de **SPropValue** contiene la marca de bit MV_FLAG, la devolución probable es MAPI_E_TOO_COMPLEX. 
  
Para obtener más información acerca de la estructura **SPropertyRestriction** , consulte [About Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Vea también

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [Estructuras MAPI](mapi-structures.md)

