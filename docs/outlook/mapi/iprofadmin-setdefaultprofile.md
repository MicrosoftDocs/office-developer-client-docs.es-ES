---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 44be43864d943257520f27297e5754a4978c568d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439628"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece o borra el perfil predeterminado de un cliente.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpszProfileName_
  
> [in] Puntero al nombre del perfil que se convertirá en el valor predeterminado o NULL. Establecer  _lpszProfileName_ en NULL indica que **SetDefaultProfile** debe quitar el perfil predeterminado existente, dejando al cliente sin un valor predeterminado. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de cadena a la que  _apunta lpszProfileName_. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> El nombre del perfil está en formato Unicode. Si no MAPI_UNICODE marca, el nombre del perfil está en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Un perfil predeterminado se estableció o eliminó correctamente.
    
MAPI_E_NOT_FOUND 
  
> El perfil especificado no existe.
    
## <a name="remarks"></a>Comentarios

El **método IProfAdmin::SetDefaultProfile** establece un perfil determinado como perfil predeterminado del cliente o borra el perfil predeterminado actual. El perfil predeterminado es el perfil que se usa automáticamente cada vez que el cliente inicia una sesión MAPI. **SetDefaultProfile** también establece la propiedad del nuevo perfil predeterminado **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) en TRUE.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para iniciar una sesión con el perfil predeterminado, pase la marca MAPI_USE_DEFAULT a la [función MAPILogonEx.](mapilogonex.md) 
  
## <a name="see-also"></a>Vea también



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Propiedad canónica PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

