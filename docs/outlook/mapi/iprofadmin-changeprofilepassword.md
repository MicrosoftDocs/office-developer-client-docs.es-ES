---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 41066d4418760a676fbc02241bfc12d83275da9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573001"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En desuso. Cambia la contraseña de un perfil.
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpszProfileName_
  
> [entrada] Un puntero al nombre del perfil asociado con la contraseña que se va a cambiar.
    
 _lpszOldPassword_
  
> [entrada] Un puntero a la contraseña actual.
    
 _lpszNewPassword_
  
> [entrada] Un puntero a la nueva contraseña.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de las cadenas que se pasan en. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> El nombre del perfil y las contraseñas están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., estas cadenas se encuentran en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Si se llama a este método, devolverá S_OK. Sin embargo, no se realizará ninguna acción.
    
## <a name="remarks"></a>Comentarios

No use este método. MAPI no admite las contraseñas para los perfiles.
  
## <a name="see-also"></a>Recursos adicionales



[IProfAdmin : IUnknown](iprofadminiunknown.md)

