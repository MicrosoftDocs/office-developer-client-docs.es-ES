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
ms.openlocfilehash: 9748229799641d62b1649491c432f10164b49192
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820752"
---
# <a name="srestriction"></a>SRestriction

  
  
**Hace referencia a**: Outlook 
  
Describe un filtro para limitar la vista de una tabla a las filas determinadas. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
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
  
> Una restricción **y** que se aplica una operación **AND** bit a bit a una restricción. 
    
RES_BITMASK 
  
> Una restricción de la máscara de bits que se aplica una máscara de bits para un valor de la propiedad.
    
RES_COMMENT 
  
> Una restricción de comentario, que asocia un comentario a una restricción.
    
RES_COMPAREPROPS 
  
> Restricción de comparación de propiedad, que compara dos valores de propiedad.
    
RES_CONTENT 
  
> Una restricción de contenido, que busca un valor de la propiedad de contenido específico.
    
RES_EXIST 
  
> Una restricción existe, que determina si se admite una propiedad.
    
RES_NOT 
  
> Una **no** restricción, que se aplica una operación **NOT** lógica a una restricción. 
    
RES_OR 
  
> Una restricción **o** , que se aplica una operación **OR** lógica a una restricción. 
    
RES_PROPERTY 
  
> Una restricción de propiedad, que determina si un valor de propiedad coincide con un valor determinado.
    
RES_SIZE 
  
> Una restricción de tamaño, que determina si un valor de la propiedad es un determinado tamaño.
    
RES_SUBRESTRICTION 
  
> Una restricción de objeto subcaracterística, que se aplica una restricción a los datos adjuntos o los destinatarios de un mensaje.
    
 **res**
  
> Unión de las estructuras de restricción que describe el filtro que se aplique. La estructura específica incluida en el miembro **rec** depende del valor del miembro **rt** . La asignación entre el tipo de restricción y la estructura se muestra en la siguiente tabla. 
    
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

Los clientes usan una estructura **SRestriction** para limitar el número y el tipo de filas en la vista de una tabla y para buscar mensajes específicos en una carpeta. Para imponer la limitación en una tabla, los clientes llaman [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md). Para imponer la limitación en una carpeta, los clientes llaman (método) [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) de la carpeta. 
  
Para obtener información acerca de cómo usar restricciones con tablas, vea [Acerca de las restricciones](about-restrictions.md). 
  
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

