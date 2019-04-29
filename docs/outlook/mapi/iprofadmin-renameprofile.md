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

## <a name="parameters"></a>Parameters

 _lpszOldProfileName_
  
> a Un puntero al nombre actual del perfil al que se va a cambiar el nombre.
    
 _lpszOldPassword_
  
> a Siempre NULL.
    
 _lpszNewProfileName_
  
> a Un puntero al nuevo nombre del perfil al que se va a cambiar el nombre.
    
 _ulUIParam_
  
> a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que muestra este método. 
    
 _ulFlags_
  
> a Siempre NULL.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se cambió el nombre del perfil correctamente.
    
MAPI_E_LOGON_FAILED 
  
> La contraseña del perfil es incorrecta.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El método **IProfAdmin:: RenameProfile** asigna un nuevo nombre a un perfil, si tiene uno. Si el perfil al que se va a cambiar el nombre lo está usando un cliente cuando se llama a **RenameProfile** , **RenameProfile** marca el perfil y Devuelve S_OK en lugar de intentar la operación de cambio de nombre mientras el perfil está en uso. Cuando el perfil ya no se usa, **RenameProfile** le asigna el nuevo nombre. 
  
Los nombres antiguos y nuevos del perfil pueden tener hasta 64 caracteres de longitud y pueden incluir los siguientes caracteres:
  
- Todos los caracteres alfanuméricos, incluidos los caracteres de énfasis y el carácter de subrayado.
    
- Espacios insertados, pero no espacios iniciales ni finales.
    
_LpszPassword_ siempre debe ser null o un puntero a una cadena de longitud cero. 
  
## <a name="see-also"></a>Ver también



[IProfAdmin : IUnknown](iprofadminiunknown.md)

