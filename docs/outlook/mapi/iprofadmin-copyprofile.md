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
ms.openlocfilehash: cd70f5ee7b58bdf0b1fd61b1056bfc77e3e35992
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817876"
---
# <a name="iprofadmincopyprofile"></a>IProfAdmin::CopyProfile

  
  
**Hace referencia a**: Outlook 
  
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
  
> [entrada] Un puntero al nombre del perfil que desea copiar.
    
 _lpszOldPassword_
  
> [entrada] Un puntero a la contraseña del perfil que desea copiar.
    
 _lpszNewProfileName_
  
> [entrada] Un puntero al nuevo nombre del perfil copiado.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se copia el perfil. Se pueden establecer los siguientes indicadores:
    
MAPI_DIALOG 
  
> Muestra un cuadro de diálogo que solicita al usuario la contraseña correcta del perfil para copiar. Si no se establece este marcador, no se muestra ningún cuadro de diálogo.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El perfil se ha copiado correctamente.
    
MAPI_E_ACCESS_DENIED 
  
> El nuevo nombre del perfil es el mismo que el de un perfil existente.
    
MAPI_E_LOGON_FAILED 
  
> La contraseña para el perfil copiar es incorrecta y no se pudo mostrar un cuadro de diálogo al usuario para solicitar la contraseña correcta porque de MAPI_DIALOG no se ha establecido en el parámetro _ulFlags indicado_ . 
    
MAPI_E_NOT_FOUND 
  
> No existe el perfil especificado.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El método **IProfAdmin::CopyProfile** hace una copia del perfil que señala _lpszOldProfileName_, póngale el nombre que señala _lpszNewProfileName_. Copiar un perfil de deja la copia con la misma contraseña que el original.
  
El nombre de la copia, su contraseña y el perfil original puede tener hasta 64 caracteres de longitud y puede incluir los siguientes caracteres:
  
- Todos los caracteres alfanuméricos, incluidos los caracteres de énfasis y el carácter de subrayado.
    
- Espacios incrustados, pero no espacios al principio o al final.
    
No se admiten contraseñas de perfiles en todos los sistemas operativos. En los sistemas operativos que no admiten las contraseñas de perfil, _lpszOldPassword_ puede ser NULL o un puntero a una cadena de longitud cero. 
  
Si _lpszOldPassword_ se establece en NULL, el perfil que se va a copiar requiere una contraseña, y se establece la marca MAPI_DIALOG; se muestra un cuadro de diálogo que solicita al usuario que proporcione la contraseña. Si es necesaria, una contraseña, pero _lpszOldPassword_ se establece en NULL y no se establece la marca MAPI_DIALOG, **CopyProfile** devuelve MAPI_E_LOGON_FAILED. 
  
## <a name="see-also"></a>Vea también



[IProfAdmin : IUnknown](iprofadminiunknown.md)

