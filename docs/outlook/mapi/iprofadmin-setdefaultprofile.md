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
ms.openlocfilehash: af695d55cdd5f8d7e24d7e60e6eebaf03868b03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587708"
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

## <a name="parameters"></a>Parámetros

 _lpszProfileName_
  
> [entrada] Un puntero al nombre del perfil que va a convertirse en el valor predeterminado o NULL. Si el valor _lpszProfileName_ NULL indica que **SetDefaultProfile** debe quitar el perfil predeterminado existente, dejando al cliente sin un valor predeterminado. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de la cadena indicada por _lpszProfileName_. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> El nombre del perfil está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., el nombre del perfil está en formato ANSI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Un perfil predeterminado se establece o se quitó correctamente.
    
MAPI_E_NOT_FOUND 
  
> No existe el perfil especificado.
    
## <a name="remarks"></a>Comentarios

El método **IProfAdmin::SetDefaultProfile** establece un perfil determinado como el perfil del cliente predeterminado o borra el perfil predeterminado actual. El perfil predeterminado es el perfil que se usa automáticamente cada vez que el cliente inicia una sesión MAPI. **SetDefaultProfile** también establece la propiedad de **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) del perfil predeterminado nuevo en TRUE.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para iniciar una sesión con el perfil predeterminado, pase el indicador MAPI_USE_DEFAULT a la función [MAPILogonEx](mapilogonex.md) . 
  
## <a name="see-also"></a>Recursos adicionales



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Propiedad canónica PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

