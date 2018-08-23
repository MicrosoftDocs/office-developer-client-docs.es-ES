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
ms.openlocfilehash: a8f4e62a8eb1b5e61cb0223c66b921e15ab9423b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577684"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de atributos para las propiedades de un objeto. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage.h  <br/> |
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
  
> Recuento de atributos de la propiedad en el miembro **aPropAttr** . 
    
 **aPropAttr**
  
> Una matriz de atributos de la propiedad. Los valores válidos para los atributos son los siguientes:
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>Comentarios

La estructura **SPropAttrArray** se usa en los objetos de datos de propiedad que implementan el [IPropData: IMAPIProp](ipropdataimapiprop.md) interfaz. También se usa la implementación de MAPI de [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) es decir, en función de almacenamiento estructurado. 
  
## <a name="see-also"></a>Recursos adicionales



[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[Estructuras MAPI](mapi-structures.md)

