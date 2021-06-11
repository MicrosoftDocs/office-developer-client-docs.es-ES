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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409149"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  
> Número de versión de la estructura. El **miembro ulVersion** se usa para la expansión futura y debe establecerse en MAPI_ERROR_VERSION, que actualmente se define como cero. 
    
 **lpszError**
  
> Puntero a una cadena que describe el error. Esta cadena tendrá un formato Unicode si el parámetro  _ulFlags_ del método en el que se usa esta estructura se establece en MAPI_UNICODE. 
    
 **lpszComponent**
  
> Puntero a una cadena que describe el componente que generó el error. Esta cadena tendrá un formato Unicode si el parámetro  _ulFlags_ del método en el que se usa esta estructura se establece en MAPI_UNICODE. 
    
 **ulLowLevelError**
  
> Valor de error de nivel bajo que solo se usa cuando el error que se va a devolver es de nivel bajo.
    
 **ulContext**
  
> Valor que representa la ubicación en el componente al que apunta el **miembro lpszComponent** que identifica dónde se produjo el error. 
    
## <a name="remarks"></a>Comentarios

La **estructura MAPIERROR** se usa para describir la información de error. Los clientes y proveedores de servicios pasan un puntero a una estructura **MAPIERROR** en el parámetro _lppMAPIError_ del [método IMAPIProp::GetLastError.](imapiprop-getlasterror.md) **GetLastError** devuelve información sobre el error anterior que se ha producido en un objeto. Los autores de llamadas **de GetLastError** liberan la memoria de la estructura **MAPIERROR** llamando a [MAPIFreeBuffer](mapifreebuffer.md).
  
El **miembro lpszComponent** se puede usar para asignar el archivo de ayuda del componente, si existe uno. Los proveedores de servicios deben limitar el tamaño de la cadena de componente a 30 caracteres para que se pueda mostrar fácilmente en un cuadro de diálogo. El **miembro ulContext** también se puede usar para hacer referencia a un tema de ayuda en línea para obtener errores comunes. 
  
Dado que los proveedores de servicios no son necesarios para proporcionar información de error detallada, los clientes no deben esperar que ninguno de los miembros de la estructura **MAPIERROR** que se devuelve contengan datos válidos. Sin embargo, como mínimo MAPI recomienda encarecidamente que los proveedores especifiquen información en los **miembros lpszComponent** **y ulContext.** 
  
Para obtener más información sobre el control de errores en MAPI, vea [Control de errores](error-handling-in-mapi.md).
  
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

