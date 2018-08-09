---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c94c60cf9ff1adbe2b54bd85b228e21b4be0e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817887"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**Hace referencia a**: Outlook 
  
Asigna un nombre nuevo a un perfil.
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpszOldProfileName_
  
> [entrada] Un puntero al nombre del perfil para cambiar el nombre actual.
    
 _lpszOldPassword_
  
> [entrada] Siempre es NULL.
    
 _lpszNewProfileName_
  
> [entrada] Un puntero al nuevo nombre del perfil para cambiar el nombre.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método. 
    
 _ulFlags_
  
> [entrada] Siempre es NULL.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se cambió correctamente el perfil.
    
MAPI_E_LOGON_FAILED 
  
> La contraseña de perfil es incorrecta.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El método **IProfAdmin::RenameProfile** asigna un nuevo nombre a un perfil, si tiene uno. Si el perfil para cambiar el nombre está en uso por un cliente cuando se llama a **RenameProfile** , **RenameProfile** marca el perfil y devuelve S_OK en lugar de intentar la operación de cambio de nombre mientras el perfil está en uso. Cuando ya no se usa el perfil, **RenameProfile** se asigna el nombre nuevo. 
  
Los nombres antiguos y nuevos del perfil pueden tener hasta 64 caracteres de longitud y pueden incluir los siguientes caracteres:
  
- Todos los caracteres alfanuméricos, incluidos los caracteres de énfasis y el carácter de subrayado.
    
- Espacios incrustados, pero no espacios al principio o al final.
    
El _lpszPassword_ siempre debe ser NULL o un puntero a una cadena de longitud cero. 
  
## <a name="see-also"></a>Vea también



[IProfAdmin : IUnknown](iprofadminiunknown.md)

