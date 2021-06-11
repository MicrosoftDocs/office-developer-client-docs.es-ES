---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424122"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra una aplicación cliente en una sesión con el sistema de mensajería. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Controla la ventana en la que el cuadro de diálogo de inicio de sesión es modal. Si no aparece ningún cuadro de diálogo durante la llamada, se omite el parámetro _ulUIParam._ Este parámetro puede ser cero. 
    
 _lpszProfileName_
  
> [in] Puntero a una cadena que contiene el nombre del perfil que se usará cuando el usuario inicie sesión. Esta cadena está limitada a 64 caracteres.
    
 _lpszPassword_
  
> [in] Puntero a una cadena que contiene la contraseña del perfil. El  _parámetro lpszPassword_ debe ser NULL. 
    
 _flFlags_
  
> [in] Máscara de bits de las marcas que se usan para controlar cómo se realiza el inicio de sesión. Se pueden establecer las siguientes marcas:
    
MAPI_ALLOW_OTHERS 
  
> Se debe devolver la sesión compartida, lo que permite a los clientes posteriores obtener la sesión sin proporcionar credenciales de usuario. 
    
MAPI_BG_SESSION
  
> Inicie sesión en una sesión y ejecute cualquier operación en segundo plano. En general, si un cliente tiene la intención de realizar el procesamiento en un subproceso en segundo plano o en un proceso independiente de una manera discreta para el subproceso en primer plano, debe llamar con la marca MAPI_BG_SESSION. Una aplicación cliente como un motor de indización o abrir un archivo de carpetas personales (PST) para el acceso de tipo en segundo plano son algunos ejemplos de dónde usar MAPI_BG_SESSION. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> El perfil predeterminado no debe usarse y el usuario debe ser necesario para proporcionar un perfil. 
    
MAPI_EXTENDED 
  
> Inicie sesión con funcionalidades extendidas. Esta marca siempre debe establecerse.
    
MAPI_FORCE_DOWNLOAD 
  
> Se debe intentar descargar todos los mensajes del usuario antes de devolverlos. Si no MAPI_FORCE_DOWNLOAD marca, los mensajes se pueden descargar en segundo plano después de que la llamada a MAPILogonEx devuelva. 
    
MAPI_LOGON_UI 
  
> Si es necesario, se debe mostrar un cuadro de diálogo para solicitar al usuario información de inicio de sesión. Cuando no MAPI_LOGON_UI marca de inicio de sesión, el cliente que llama no muestra un cuadro de diálogo de inicio de sesión y devuelve un valor de error si el usuario no ha iniciado sesión.
    
MAPI_NEW_SESSION 
  
> Se debe intentar crear una nueva sesión MAPI en lugar de adquirir la sesión compartida. Si no MAPI_NEW_SESSION marca, MAPILogonEx usa una sesión compartida existente incluso si el parámetro  _lpszprofileName_ no es NULL. 
    
MAPI_NO_MAIL 
  
> MAPI no debe informar a la cola MAPI de la existencia de la sesión. El resultado es que no se pueden enviar ni recibir mensajes en la sesión excepto a través de un par de almacenamiento y transporte estrechamente acoplados. Un cliente que llama establece esta marca si actúa como agente, si se debe realizar el trabajo de configuración o si el cliente está explorando los almacenes de mensajes disponibles. 
    
MAPI_NT_SERVICE 
  
> El autor de la llamada se ejecuta como Windows servicio. Los autores de llamadas que no se ejecutan como servicio Windows no deben establecer esta marca; Los autores de llamadas que se ejecutan como servicio deben establecer esta marca. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx debe mostrar un cuadro de diálogo de configuración para cada servicio de mensajes del perfil. Los cuadros de diálogo se muestran después de elegir el perfil, pero antes de iniciar sesión en cualquier servicio de mensajes. El cuadro de diálogo común MAPI para el inicio de sesión también contiene una casilla que solicita la misma operación. 
    
MAPI_TIMEOUT_SHORT 
  
> El inicio de sesión debe producir un error si se bloquea durante más de unos segundos. 
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI. 
    
MAPI_USE_DEFAULT 
  
> El subsistema de mensajería debe sustituir el nombre de perfil del perfil predeterminado para el _parámetro lpszProfileName._ El MAPI_EXPLICIT_PROFILE se omite a menos  _que lpszProfileName_ sea NULL o vacío. 
    
 _lppSession_
  
> [salida] Puntero a un puntero a la interfaz de sesión MAPI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El inicio de sesión se ha correcto.
    
MAPI_E_LOGON_FAILED 
  
> El inicio de sesión no se ha hecho correctamente, ya sea porque uno o varios de los parámetros de MAPILogonEx no eran válidos o porque ya había demasiadas sesiones abiertas.
    
MAPI_E_TIMEOUT 
  
> MAPI serializa todos los inicios de sesión a través de un mutex. Esto se devuelve si se MAPI_TIMEOUT_SHORT marca y otro subproceso mantiene la función mutex. 
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente MAPI llaman a la función MAPILogonEx para iniciar sesión en una sesión con el sistema de mensajería. Todas las cadenas que se pasan y devuelven a y desde llamadas MAPI terminan en null y deben especificarse en el conjunto de caracteres actual o en la página de código del sistema operativo del proveedor o cliente de llamadas.
  
El  _parámetro lpszProfileName_ se omite si hay una sesión anterior existente que llamó a MapiLogonEx con el conjunto de marcas MAPI_ALLOW_OTHERS y si no se establece la marca MAPI_NEW_SESSION. Si el parámetro  _lpszProfileName_ es NULL o apunta a una cadena vacía y el parámetro  _flFlags_ incluye la marca MAPI_LOGON_UI, la función MAPILogonEx genera un cuadro de diálogo de inicio de sesión que tiene un campo vacío para el nombre del perfil. 
  
Al iniciar sesión en un perfil específico, un cliente debe pasar la marca MAPI_NEW_SESSION a MAPILogonEx además del nombre del perfil. De lo contrario, si otro cliente ha establecido una sesión compartida iniciando sesión con MAPI_ALLOW_OTHERS, el cliente iniciará sesión en la sesión compartida en lugar del perfil solicitado. 
  
La MAPI_EXPLICIT_PROFILE no hace que se use el nombre de perfil predeterminado cuando  _lpszProfileName_ es NULL o está vacío a menos que la marca MAPI_USE_DEFAULT esté presente. 
  
La MAPI_NO_MAIL tiene varios efectos que provocan lo siguiente cuando no se usa la cola MAPI:
  
- La cola MAPI no puede enviar ni entregar mensajes durante esta sesión. Solo los proveedores de almacenamiento y transporte estrechamente acoplados pueden enviar y entregar mensajes. 
    
- Es posible que los almacenes basados en el servidor aún envíen o entreguen mensajes. 
    
- Los mensajes enviados o entregados por almacenes basados en servidor no son procesados por ningún proveedor de enlaces. 
    
- Las opciones por mensaje y por destinatario para transportes no están disponibles. 
    
- La tabla de estado no contiene entradas para proveedores de transporte y ninguna funcionalidad de transporte dependiente de objetos de estado (como la configuración) no está disponible. 
    
- La fila de cola de mensajes de la tabla de estado contiene STATUS_FAILURE valor. 
    
- Se permiten los inicios de sesión con piggybacked, pero esos inicios de sesión no hacen que el inicio de sesión anterior reciba actualizaciones de objetos de estado. 
    
Un servicio siempre debe iniciar sesión con la MAPI_NO_MAIL marca. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::MAPILogonEx  <br/> |MFCMAPI usa el método MAPILogonEx para iniciar sesión en MAPI.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

