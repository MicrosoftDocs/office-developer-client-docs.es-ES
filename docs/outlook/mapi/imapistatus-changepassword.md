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
ms.openlocfilehash: 2c824b6b994bfb31b5e6ac7fed0eeae88c47cdba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328283"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Modifica la contraseña de un proveedor de servicios sin mostrar una interfaz de usuario. Este método es compatible opcionalmente con los objetos de estado que implementan los proveedores de servicios.
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpOldPass_
  
> a Un puntero a la contraseña antigua.
    
 _lpNewPass_
  
> a Un puntero a la nueva contraseña.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla el formato de las contraseñas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las contraseñas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las contraseñas están en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La modificación de la contraseña se realizó correctamente.
    
MAPI_E_NO_ACCESS 
  
> La contraseña anterior a la que apunta _lpOldPass_ no es válida. 
    
MAPI_E_NO_SUPPORT 
  
> El objeto status no admite esta operación, como indica la ausencia de la marca STATUS_CHANGE_PASSWORD en la propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del objeto de estado.
    
## <a name="remarks"></a>Comentarios

No todos los objetos status admiten el método **IMAPIStatus:: ChangePassword** . Solo la admiten los proveedores de servicios que requieren que los clientes escriban una contraseña. Ninguno de los objetos de estado que implementa MAPI admiten la operación de cambio de contraseña. 
  
 **ChangePassword** modifica una contraseña mediante programación, sin interacción del usuario. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Los proveedores de transporte remoto implementan **ChangePassword** tal y como se especifica aquí. No hay ninguna consideración especial. 
  
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

