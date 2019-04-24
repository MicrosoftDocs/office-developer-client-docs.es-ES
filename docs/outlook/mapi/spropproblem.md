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
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357851"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un error relacionado con una operación que implica una propiedad.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Índice en una matriz de etiquetas de propiedad.
    
 **ulPropTag**
  
> Etiqueta de propiedad de la propiedad que tiene el error.
    
 **SCODE**
  
> Valor de error que describe el problema con la propiedad. Este valor puede ser cualquier valor [SCODE](scode.md) de MAPI. 
    
## <a name="remarks"></a>Comentarios

Se devuelve una matriz de estructuras **SPropProblem** desde los métodos siguientes: 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
Una estructura **SPropProblem** contiene un valor de error **SCODE** que es el resultado de una operación que intenta modificar o eliminar una propiedad MAPI. 
  
Para obtener más información sobre cómo funciona la estructura **SPropProblem** con los errores relacionados con las propiedades, consulte [MAPI con nombre de propiedades](mapi-named-properties.md). 
  
## <a name="see-also"></a>Vea también



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[Estructuras MAPI](mapi-structures.md)

