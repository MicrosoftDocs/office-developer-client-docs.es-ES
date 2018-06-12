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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: c57f945d16cc80c637b1a4074b25f9cf1fb1edc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817892"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**Se aplica a**: Outlook 
  
En desuso. Cambia la contraseña de un perfil.
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Sintaxis

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
    
## <a name="remarks"></a>Notas

No use este método. MAPI no admite las contraseñas para los perfiles.
  
## <a name="see-also"></a>Ver también



[IProfAdmin: IUnknown](iprofadminiunknown.md)

