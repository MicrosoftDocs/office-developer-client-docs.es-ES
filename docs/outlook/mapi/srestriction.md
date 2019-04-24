---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341744"
---
# <a name="srestriction"></a>SRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un filtro para limitar la vista de una tabla a filas específicas. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SRestriction
{
  ULONG rt;
  union
  {
    SComparePropsRestriction resCompareProps;
    SAndRestriction resAnd;
    SOrRestriction resOr;
    SNotRestriction resNot;
    SContentRestriction resContent;
    SPropertyRestriction resProperty;
    SBitMaskRestriction resBitMask;
    SSizeRestriction resSize;
    SExistRestriction resExist;
    SSubRestriction resSub;
    SCommentRestriction resComment;
  } res;
} SRestriction;

```

## <a name="members"></a>Members

 **RT**
  
> El tipo de restricción. Los valores posibles son los siguientes: 
    
RES_AND 
  
> Una restricción **and** , que aplica una operación **** and bit a bit a una restricción. 
    
RES_BITMASK 
  
> Una restricción de máscara de máscara, que aplica una máscara de máscara a un valor de propiedad.
    
RES_COMMENT 
  
> Una restricción de comentario, que asocia un comentario con una restricción.
    
RES_COMPAREPROPS 
  
> Una restricción de comparación de propiedades, que compara dos valores de propiedad.
    
RES_CONTENT 
  
> Una restricción de contenido, que busca contenido específico en un valor de propiedad.
    
RES_EXIST 
  
> Una restricción EXISTS, que determina si se admite una propiedad.
    
RES_NOT 
  
> Una restricción **Not** que aplica una operación **Not** lógica a una restricción. 
    
RES_OR 
  
> Una restricción **or** que aplica una operación OR **** lógica a una restricción. 
    
RES_PROPERTY 
  
> Una restricción de propiedad, que determina si un valor de propiedad coincide con un valor determinado.
    
RES_SIZE 
  
> Una restricción de tamaño, que determina si un valor de propiedad es un tamaño determinado.
    
RES_SUBRESTRICTION 
  
> Una restricción de subobjeto, que aplica una restricción a los datos adjuntos o destinatarios de un mensaje.
    
 **res**
  
> Unión de estructuras de restricción que describen el filtro que se va a aplicar. La estructura específica que se incluye en el miembro **res** depende del valor del miembro **RT** . La asignación entre el tipo de restricción y la estructura se muestra en la siguiente tabla. 
    
|||
|:-----|:-----|
|**Tipo de restricción** <br/> |**Estructura de restricción** <br/> |
|RES_AND  <br/> |[SAndRestriction](sandrestriction.md) <br/> |
|RES_BITMASK  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |
|RES_COMMENT  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |
|RES_COMPAREPROPS  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |
|RES_CONTENT  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |
|RES_EXIST  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |
|RES_NOT  <br/> |[SNotRestriction](snotrestriction.md) <br/> |
|RES_OR  <br/> |[SOrRestriction](sorrestriction.md) <br/> |
|RES_PROPERTY  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |
|RES_SIZE  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |
|RES_SUBRESTRICTION  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a>Comentarios

Los clientes usan una estructura **SRestriction** para limitar el número y el tipo de filas en su vista de una tabla y para buscar mensajes específicos en una carpeta. Para imponer la limitación en una tabla, los clientes llaman a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md). Para imponer la limitación en una carpeta, los clientes llaman al método [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) de la carpeta. 
  
Para obtener información acerca de cómo usar restricciones con tablas, consulte [About Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Vea también



[SAndRestriction](sandrestriction.md)
  
[SBitMaskRestriction](sbitmaskrestriction.md)
  
[SCommentRestriction](scommentrestriction.md)
  
[SComparePropsRestriction](scomparepropsrestriction.md)
  
[SContentRestriction](scontentrestriction.md)
  
[SExistRestriction](sexistrestriction.md)
  
[SNotRestriction](snotrestriction.md)
  
[SOrRestriction](sorrestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SSizeRestriction](ssizerestriction.md)
  
[SSubRestriction](ssubrestriction.md)


[Estructuras MAPI](mapi-structures.md)

