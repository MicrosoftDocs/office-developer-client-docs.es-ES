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
ms.openlocfilehash: 682e75c4e0a2f60dbd46a13b0b737ca4a8e18f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345783"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona información detallada sobre un error, generado normalmente por el sistema operativo, MAPI o un proveedor de servicios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Número de versión de la estructura. El miembro **ulVersion** se usa para la expansión futura y debe establecerse en MAPI_ERROR_VERSION, que se define actualmente como cero. 
    
 **lpszError**
  
> Puntero a una cadena que describe el error. Esta cadena estará en formato Unicode si el parámetro _ulFlags_ del método en el que se usa esta estructura se establece en MAPI_UNICODE. 
    
 **lpszComponent**
  
> Puntero a una cadena que describe el componente que ha generado el error. Esta cadena estará en formato Unicode si el parámetro _ulFlags_ del método en el que se usa esta estructura se establece en MAPI_UNICODE. 
    
 **ulLowLevelError**
  
> Valor de error de nivel bajo que se usa solo cuando el error que se va a devolver es de bajo nivel.
    
 **ulContext**
  
> Que representa la ubicación en el componente apuntado por el miembro **lpszComponent** que identifica dónde se produjo el error. 
    
## <a name="remarks"></a>Comentarios

La estructura **MAPIERROR** se usa para describir la información de error. Los clientes y los proveedores de servicios pasan un puntero a una estructura **MAPIERROR** en el parámetro _LppMAPIError_ del método [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) . **GetLastError** devuelve información sobre el error anterior que se ha producido en un objeto. Los llamadores de **GetLastError** liberan la memoria para la estructura **MAPIERROR** llamando a [MAPIFreeBuffer](mapifreebuffer.md).
  
El miembro **lpszComponent** se puede usar para asignar el archivo de ayuda del componente, si existe alguno. Los proveedores de servicios deben limitar el tamaño de la cadena del componente a 30 caracteres para que se pueda mostrar fácilmente en un cuadro de diálogo. El miembro **ulContext** también se puede usar para hacer referencia a un tema de la ayuda en pantalla para errores comunes. 
  
Debido a que no es necesario que los proveedores de servicios proporcionen información detallada sobre los errores, los clientes no deben esperar que los miembros de la estructura **MAPIERROR** devuelvan datos válidos. Sin embargo, en un MAPI mínimo recomienda que los proveedores especifiquen información en los miembros **lpszComponent** y **ulContext** . 
  
Para obtener más información sobre el control de errores en MAPI, vea [control de errores](error-handling-in-mapi.md).
  
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

