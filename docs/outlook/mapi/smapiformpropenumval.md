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
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435414"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Asigna un valor entero enumerado a un nombre para mostrar para ese valor. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm. h  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a>Members

 **pszDisplayName**
  
> Cadena que contiene el nombre para mostrar del valor especificado en el miembro **nVal** . 
    
 **nVal**
  
> Un valor de enumeración para el nombre para mostrar al que apunta el miembro **pszDisplayName** . 
    
## <a name="remarks"></a>Comentarios

Cuando un usuario selecciona un nombre para mostrar de un formulario, el valor de enumeración correspondiente del nombre se almacena mediante la implementación de la interfaz [IMAPIProp](imapipropiunknown.md) asociada con el formulario. 
  
## <a name="see-also"></a>Ver también



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

