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
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419523"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Asigna un nuevo nombre a un perfil.
  
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
  
> [entrada] Puntero al nombre actual del perfil para cambiar el nombre.
    
 _lpszOldPassword_
  
> [entrada] Siempre NULL.
    
 _lpszNewProfileName_
  
> [entrada] Puntero al nuevo nombre del perfil para cambiar el nombre.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método. 
    
 _ulFlags_
  
> [entrada] Siempre NULL.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se cambió el nombre del perfil correctamente.
    
MAPI_E_LOGON_FAILED 
  
> La contraseña de perfil es incorrecta.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón** Cancelar de un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El **método IProfAdmin::RenameProfile** asigna un nuevo nombre a un perfil, si lo tiene. Si un cliente usa el perfil para cambiar el nombre cuando se llama a **RenameProfile,** **RenameProfile** marca el perfil y devuelve S_OK en lugar de intentar la operación de cambio de nombre mientras el perfil está en uso. Cuando el perfil ya no se usa, **RenameProfile** le asigna el nuevo nombre. 
  
Los nombres antiguos y nuevos del perfil pueden tener hasta 64 caracteres de longitud y pueden incluir los siguientes caracteres:
  
- Todos los caracteres alfanuméricos, incluidos los caracteres de énfrica y el carácter de subrayado.
    
- Espacios incrustados, pero no espacios iniciales o finales.
    
_LpszPassword siempre_ debe ser NULL o un puntero a una cadena de longitud cero. 
  
## <a name="see-also"></a>Consulte también



[IProfAdmin : IUnknown](iprofadminiunknown.md)

