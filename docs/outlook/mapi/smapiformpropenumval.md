---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2c49a17389a9bfc998f892e0becf96dca4cd773f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578720"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Asigna un valor entero enumerado a un nombre para mostrar para ese valor. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a>Members

 **pszDisplayName**
  
> Cadena que contiene el nombre para mostrar para el valor especificado en el miembro **nVal** . 
    
 **nVal**
  
> Un valor de enumeración para el nombre para mostrar que señala el miembro **pszDisplayName** . 
    
## <a name="remarks"></a>Comentarios

Cuando un usuario selecciona un nombre para mostrar de un formulario, se almacena valor de enumeración correspondiente del nombre mediante el uso de la implementación de la interfaz de [IMAPIProp](imapipropiunknown.md) que está asociada con el formulario. 
  
## <a name="see-also"></a>Vea también



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

