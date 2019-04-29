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
ms.openlocfilehash: c7124c8e3f2ced66d303321ff7aee8592a723a2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420244"
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

## <a name="parameters"></a>Parameters

 _lpszProfileName_
  
> a Un puntero al nombre del perfil asociado con la contraseña que se va a cambiar.
    
 _lpszOldPassword_
  
> a Un puntero a la contraseña actual.
    
 _lpszNewPassword_
  
> a Un puntero a la nueva contraseña.
    
 _ulFlags_
  
> a Una máscara de bits de marcadores que controla el tipo de las cadenas pasadas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> El nombre del perfil y las contraseñas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, estas cadenas están en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Si se llama a este método, devolverá S_OK. Sin embargo, no se llevará a cabo ninguna acción.
    
## <a name="remarks"></a>Comentarios

No use este método. MAPI no admite contraseñas para los perfiles.
  
## <a name="see-also"></a>Ver también



[IProfAdmin : IUnknown](iprofadminiunknown.md)

