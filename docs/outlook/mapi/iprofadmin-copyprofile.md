---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437241"
---
# <a name="iprofadmincopyprofile"></a>IProfAdmin::CopyProfile

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia un perfil.
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpszOldProfileName_
  
> [entrada] Puntero al nombre del perfil que se copiará.
    
 _lpszOldPassword_
  
> [entrada] Puntero a la contraseña del perfil que se copiará.
    
 _lpszNewProfileName_
  
> [entrada] Puntero al nuevo nombre del perfil copiado.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se copia el perfil. Se pueden establecer las siguientes marcas:
    
MAPI_DIALOG 
  
> Muestra un cuadro de diálogo que solicita al usuario la contraseña correcta del perfil que se debe copiar. Si no se establece esta marca, no se muestra ningún cuadro de diálogo.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El perfil se copió correctamente.
    
MAPI_E_ACCESS_DENIED 
  
> El nuevo nombre de perfil es el mismo que el de un perfil existente.
    
MAPI_E_LOGON_FAILED 
  
> La contraseña del perfil que se va a copiar es incorrecta y no se pudo mostrar un cuadro de diálogo al usuario para solicitar la contraseña correcta porque MAPI_DIALOG no se estableció en el parámetro _ulFlags._ 
    
MAPI_E_NOT_FOUND 
  
> El perfil especificado no existe.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón** Cancelar de un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El **método IProfAdmin::CopyProfile** hace una copia del perfil al que apunta  _lpszOldProfileName_, con el nombre que apunta  _lpszNewProfileName_. Copiar un perfil deja la copia con la misma contraseña que el original.
  
El nombre del perfil original, su contraseña y la copia pueden tener una longitud de hasta 64 caracteres y pueden incluir los siguientes caracteres:
  
- Todos los caracteres alfanuméricos, incluidos los caracteres de énfrica y el carácter de subrayado.
    
- Espacios incrustados, pero no espacios iniciales o finales.
    
Las contraseñas de perfil no se admiten en todos los sistemas operativos. En sistemas operativos que no admiten contraseñas de perfil,  _lpszOldPassword_ puede ser NULL o un puntero a una cadena de longitud cero. 
  
Si  _lpszOldPassword_ se establece en NULL, el perfil que se va a copiar requiere una contraseña y se MAPI_DIALOG marca predeterminada; Se muestra un cuadro de diálogo que solicita al usuario que proporcione la contraseña. Si se requiere una contraseña, pero  _lpszOldPassword_ se establece en NULL y no se establece la marca MAPI_DIALOG, **CopyProfile** devuelve MAPI_E_LOGON_FAILED. 
  
## <a name="see-also"></a>Consulte también



[IProfAdmin : IUnknown](iprofadminiunknown.md)

