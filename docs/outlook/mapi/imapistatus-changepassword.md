---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b667f56553b717f1bc938b6ce045dbfdde8fdc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817470"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**Hace referencia a**: Outlook 
  
Modifica la contraseña de un proveedor de servicios sin mostrar la interfaz de usuario. Opcionalmente, este método se admite en los objetos de estado que implementan los proveedores de servicio.
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpOldPass_
  
> [entrada] Un puntero a la contraseña antigua.
    
 _lpNewPass_
  
> [entrada] Un puntero a la nueva contraseña.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el formato de las contraseñas. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las contraseñas están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las contraseñas están en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La modificación de la contraseña era correcta.
    
MAPI_E_NO_ACCESS 
  
> La contraseña antigua que señala _lpOldPass_ no es válida. 
    
MAPI_E_NO_SUPPORT 
  
> El objeto de estado no es compatible con esta operación, tal como se indica por la ausencia de la marca STATUS_CHANGE_PASSWORD en propiedad de **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del objeto de estado.
    
## <a name="remarks"></a>Comentarios

No todos los objetos de estado admiten el método **IMAPIStatus** . Se admite sólo por los proveedores de servicio que requieren los clientes que escribir una contraseña. Ninguno de los objetos de estado que implementa MAPI admite la operación de cambio de contraseña. 
  
 **ChangePassword** modifica una contraseña mediante programación, sin interacción del usuario. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Los proveedores de transporte remoto implementan **ChangePassword** tal como se especifica aquí. No hay ninguna consideración especial. 
  
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

