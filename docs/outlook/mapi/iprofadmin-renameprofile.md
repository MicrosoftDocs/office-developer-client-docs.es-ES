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

## <a name="parameters"></a>Parameters

 _lpszOldProfileName_
  
> [in] Puntero al nombre actual del perfil para cambiar el nombre.
    
 _lpszOldPassword_
  
> [in] Siempre NULL.
    
 _lpszNewProfileName_
  
> [in] Puntero al nuevo nombre del perfil al que se cambiará el nombre.
    
 _ulUIParam_
  
> [in] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método. 
    
 _ulFlags_
  
> [in] Siempre NULL.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El nombre del perfil se cambió correctamente.
    
MAPI_E_LOGON_FAILED 
  
> La contraseña del perfil es incorrecta.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El **método IProfAdmin::RenameProfile** asigna un nuevo nombre a un perfil, si tiene uno. Si un cliente usa el perfil para cambiar el nombre cuando se llama a **RenameProfile,** **RenameProfile** marca el perfil y devuelve S_OK en lugar de intentar la operación de cambio de nombre mientras el perfil está en uso. Cuando el perfil ya no se usa, **RenameProfile** le asigna el nuevo nombre. 
  
Los nombres antiguos y nuevos del perfil pueden tener hasta 64 caracteres y pueden incluir los siguientes caracteres:
  
- Todos los caracteres alfanuméricos, incluidos los caracteres de énfrica y el carácter de subrayado.
    
- Espacios incrustados, pero no espacios iniciales o finales.
    
_LpszPassword_ siempre debe ser NULL o un puntero a una cadena de longitud cero. 
  
## <a name="see-also"></a>Vea también



[IProfAdmin : IUnknown](iprofadminiunknown.md)

