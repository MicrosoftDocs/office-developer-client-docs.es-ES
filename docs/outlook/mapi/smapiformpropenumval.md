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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: bae750e7e940bc1417b3d225c9c81129e9da77b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820708"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Se aplica a**: Outlook 
  
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

## <a name="members"></a>Miembros

 **pszDisplayName**
  
> Cadena que contiene el nombre para mostrar para el valor especificado en el miembro **nVal** . 
    
 **nVal**
  
> Un valor de enumeración para el nombre para mostrar que señala el miembro **pszDisplayName** . 
    
## <a name="remarks"></a>Notas

Cuando un usuario selecciona un nombre para mostrar de un formulario, se almacena valor de enumeración correspondiente del nombre mediante el uso de la implementación de la interfaz de [IMAPIProp](imapipropiunknown.md) que está asociada con el formulario. 
  
## <a name="see-also"></a>Ver también



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

