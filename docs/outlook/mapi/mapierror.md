---
title: MAPIERROR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIERROR
api_type:
- COM
ms.assetid: e04c2228-aa0a-4958-b5b2-6467e93ab613
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d0ddff638e26940ea74932a8a491455f67cc8dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818243"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**Hace referencia a**: Outlook 
  
Proporciona información detallada sobre un error, normalmente generado por el sistema operativo, MAPI o un proveedor de servicios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _MAPIERROR
{
  ULONG ulVersion;
  LPSTR lpszError;
  LPSTR lpszComponent;
  ULONG ulLowLevelError;
  ULONG ulContext;
} MAPIERROR, FAR * LPMAPIERROR;

```

## <a name="members"></a>Members

 **ulVersion**
  
> Número de versión de la estructura. El miembro **ulVersion** se usa para la expansión futura y debe establecerse en MAPI_ERROR_VERSION, que actualmente se define como cero. 
    
 **lpszError**
  
> Puntero a una cadena que describe el error. Esta cadena estará en formato Unicode si se establece el parámetro _ulFlags_ al método en el que se usa esta estructura en MAPI_UNICODE.. 
    
 **lpszComponent**
  
> Puntero a una cadena que describe el componente que generó el error. Esta cadena estará en formato Unicode si se establece el parámetro _ulFlags_ al método en el que se usa esta estructura en MAPI_UNICODE.. 
    
 **ulLowLevelError**
  
> Valor de error de bajo nivel que se usa sólo cuando el error que se devuelve es bajo nivel.
    
 **ulContext**
  
> Valor que representa la ubicación en el componente que señala el miembro **lpszComponent** que identifica donde se produjo el error. 
    
## <a name="remarks"></a>Comentarios

La estructura **MAPIERROR** se usa para describir la información de error. Los clientes y proveedores de servicios de pasan un puntero a una estructura **MAPIERROR** en el parámetro _lppMAPIError_ del método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) . **GetLastError** devuelve información sobre el error anterior que se ha producido a un objeto. Los autores de llamadas de **GetLastError** libere la memoria para la estructura **MAPIERROR** mediante una llamada [MAPIFreeBuffer](mapifreebuffer.md).
  
El miembro **lpszComponent** puede utilizarse para asignar el archivo de Ayuda del componente, si lo hay. Proveedores de servicios deben limitar el tamaño de la cadena de componente a 30 caracteres para que se puede mostrar fácilmente en un cuadro de diálogo. El miembro **ulContext** también puede usarse para hacer referencia a un tema de ayuda en pantalla de los errores comunes. 
  
Debido a que los proveedores de servicio no son necesarios para proporcionar información detallada del error, los clientes no deben esperar que cualquiera de los miembros de la estructura **MAPIERROR** que se devuelven para contener datos válidos. Sin embargo, en un mínimo MAPI recomienda encarecidamente que los proveedores de especifican información en los miembros **lpszComponent** y **ulContext** . 
  
Para obtener más información acerca de control de errores en MAPI, vea [Control de errores](error-handling-in-mapi.md).
  
## <a name="see-also"></a>Vea también



[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IABProvider::Logon](iabprovider-logon.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md)
  
[IMSLogon::GetLastError](imslogon-getlasterror.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[IProfAdmin::GetLastError](iprofadmin-getlasterror.md)
  
[IProviderAdmin::GetLastError](iprovideradmin-getlasterror.md)


[Estructuras MAPI](mapi-structures.md)

