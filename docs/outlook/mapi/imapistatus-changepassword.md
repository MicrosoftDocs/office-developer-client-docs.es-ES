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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410360"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Modifica la contraseña de un proveedor de servicios sin mostrar una interfaz de usuario. Este método se admite opcionalmente en objetos de estado que los proveedores de servicios implementan.
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpOldPass_
  
> [in] Puntero a la contraseña antigua.
    
 _lpNewPass_
  
> [in] Puntero a la nueva contraseña.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el formato de las contraseñas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las contraseñas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las contraseñas están en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La modificación de contraseña se ha realizado correctamente.
    
MAPI_E_NO_ACCESS 
  
> La contraseña antigua a la que  _apunta lpOldPass_ no es válida. 
    
MAPI_E_NO_SUPPORT 
  
> El objeto status no admite esta operación, como se indica por la ausencia de la marca STATUS_CHANGE_PASSWORD en la propiedad PR_RESOURCE_METHODS **(** [PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del objeto de estado.
    
## <a name="remarks"></a>Comentarios

No todos los objetos de estado admiten el método **IMAPIStatus::ChangePassword.** Solo son compatibles con los proveedores de servicios que requieren que los clientes escriban una contraseña. Ninguno de los objetos de estado que implementa MAPI admiten la operación de cambio de contraseña. 
  
 **ChangePassword** modifica una contraseña mediante programación, sin interacción del usuario. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Los proveedores de transporte remoto **implementan ChangePassword** como se especifica aquí. No hay consideraciones especiales. 
  
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

