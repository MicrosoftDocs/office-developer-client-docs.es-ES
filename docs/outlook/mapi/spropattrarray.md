---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 55cba4f7cfb3fa8035117348b10ab1d6d3082710
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405516"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de atributos para las propiedades de un objeto. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage. h  <br/> |
|Macros relacionadas:  <br/> |[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Número de atributos de propiedad en el miembro **aPropAttr** . 
    
 **aPropAttr**
  
> Una matriz de atributos Property. Los valores válidos para los atributos son los siguientes:
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>Comentarios

La estructura **SPropAttrArray** se usa en los objetos de datos de propiedad que implementan la interfaz [IPropData: IMAPIProp](ipropdataimapiprop.md) . También se usa en la implementación de MAPI de [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) que se basa en el almacenamiento estructurado. 
  
## <a name="see-also"></a>Ver también



[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[Estructuras MAPI](mapi-structures.md)

