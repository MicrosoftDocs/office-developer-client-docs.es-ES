---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7c19cce33ec351a5627870782ebb4fe509a98be2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573288"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un error que se relacionan con una operación que implica una propiedad.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a>Members

 **ulIndex**
  
> Un índice en una matriz de etiquetas de propiedad.
    
 **ulPropTag**
  
> Etiqueta de propiedad de la propiedad que tiene el error.
    
 **SCODE**
  
> Valor de error que describe el problema con la propiedad. Este valor puede ser cualquier valor [SCODE](scode.md) de MAPI. 
    
## <a name="remarks"></a>Comentarios

Se devuelve una matriz de estructuras **SPropProblem** entre los siguientes métodos: 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
Una estructura **SPropProblem** contiene un valor de error **SCODE** que dan como resultado de una operación intenta modificar o eliminar una propiedad MAPI. 
  
Para obtener más información acerca de cómo funciona la estructura **SPropProblem** con errores relacionados con las propiedades, vea [Propiedades de nombre de MAPI](mapi-named-properties.md). 
  
## <a name="see-also"></a>Recursos adicionales



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[Estructuras MAPI](mapi-structures.md)

