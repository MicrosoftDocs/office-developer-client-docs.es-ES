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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 08782fe616fe260388cff8982dfbb09951453a00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818247"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**Se aplica a**: Outlook 
  
Los registros de una aplicación cliente de sesión en una sesión con el sistema de mensajería. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
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

## <a name="parameters"></a>Sintaxis

 _ulUIParam_
  
> [entrada] Identificador de la ventana a la que el cuadro de diálogo de inicio de sesión es modal. Si no aparece ningún cuadro de diálogo durante la llamada, se omite el parámetro _ulUIParam_ . Este parámetro puede ser cero. 
    
 _lpszProfileName_
  
> [entrada] Puntero a una cadena que contiene el nombre del perfil que desea usar cuando el usuario inicia sesión. Esta cadena está limitada a 64 caracteres.
    
 _lpszPassword_
  
> [entrada] Puntero a una cadena que contiene la contraseña del perfil. El parámetro _lpszPassword_ debe ser NULL. 
    
 _flFlags_
  
> [entrada] Máscara de bits de indicadores que se utilizan para controlar cómo se realiza el inicio de sesión. Se pueden establecer los siguientes indicadores:
    
MAPI_ALLOW_OTHERS 
  
> Debe devolverse la sesión compartida, lo que permite a los clientes posteriores para obtener la sesión sin tener que proporcionar las credenciales de usuario. 
    
MAPI_BG_SESSION
  
> Inicie sesión en una sesión y ejecutar las operaciones en segundo plano. En general, si un cliente se va a realizar el procesamiento en un subproceso de fondo o en un proceso independiente de manera que sea discreto al subproceso de primer plano, debe llamar con el indicador MAPI_BG_SESSION. Una aplicación cliente como un motor de indización o abrir un archivo de carpetas personales (PST) para el acceso de tipo de fondo son algunos ejemplos que se va a usar MAPI_BG_SESSION. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> No se debe usar el perfil predeterminado y el usuario debe ser necesarios para proporcionar un perfil. 
    
MAPI_EXTENDED 
  
> Inicie sesión con capacidades extendidas. Siempre se debe establecer este indicador.
    
MAPI_FORCE_DOWNLOAD 
  
> Se debe realizar un intento descargar todos los mensajes del usuario antes de devolverlo. Si no está establecido el indicador MAPI_FORCE_DOWNLOAD, se pueden descargar los mensajes en segundo plano después de la llamada a MAPILogonEx devuelve. 
    
MAPI_LOGON_UI 
  
> Debe mostrarse un cuadro de diálogo para preguntar al usuario para obtener información de inicio de sesión si es necesario. Cuando no está establecido el indicador MAPI_LOGON_UI, el cliente de la llamada no muestra un cuadro de diálogo de inicio de sesión y devuelve un valor de error si el usuario no ha iniciado sesión.
    
MAPI_NEW_SESSION 
  
> Para crear una nueva sesión MAPI en lugar de adquisición de la sesión compartida, se debe realizar un intento. Si no está establecido el indicador MAPI_NEW_SESSION, MAPILogonEx usa una sesión compartida existente, incluso si el parámetro _lpszprofileName_ no es nulo. 
    
MAPI_NO_MAIL 
  
> MAPI no debe informar a la cola MAPI de la existencia de la sesión. El resultado es que no hay mensajes pueden ser enviados o recibidos en la sesión excepto a través de un acoplado almacenar y par de transporte. Un cliente de la llamada establece esta marca si actúa como un agente, si el trabajo de configuración debe llevarse a cabo, o si el cliente está explorando los almacenes de mensajes disponibles. 
    
MAPI_NT_SERVICE 
  
> El autor de la llamada se ejecuta como un servicio de Windows. Autores de llamadas que no se ejecutan como un servicio de Windows no debe establecer esta marca; autores de llamadas que se ejecutan como un servicio debe establecer este indicador. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx debe mostrar un cuadro de diálogo de configuración para cada servicio de mensajes en el perfil. Una vez que se ha seleccionado el perfil, pero antes de cualquier mensaje de servicio se registra, se muestran los cuadros de diálogo. El cuadro de diálogo comunes de MAPI para el inicio de sesión también contiene una casilla de verificación que solicita la misma operación. 
    
MAPI_TIMEOUT_SHORT 
  
> El inicio de sesión debe producirá un error si bloqueado durante más de unos segundos. 
    
MAPI_UNICODE. 
  
> Las cadenas que se pasan en están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI. 
    
MAPI_USE_DEFAULT 
  
> El subsistema de mensajería debe sustituir el nombre del perfil del perfil predeterminado para el parámetro _lpszProfileName_ . El indicador MAPI_EXPLICIT_PROFILE se omite a menos que _lpszProfileName_ es NULL o está vacío. 
    
 _lppSession_
  
> [out] Puntero a un puntero a la interfaz de sesión MAPI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El inicio de sesión se ha realizado correctamente.
    
MAPI_E_LOGON_FAILED 
  
> El inicio de sesión era incorrecta, porque uno o varios de los parámetros a MAPILogonEx no eran válidos o porque ya había demasiadas sesiones abiertas.
    
MAPI_E_TIMEOUT 
  
> MAPI serializa todos los inicios de sesión a través de una exclusión mutua. Esto se devuelve si se ha establecido el indicador MAPI_TIMEOUT_SHORT y otro subproceso conserva la exclusión mutua. 
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Notas

Las aplicaciones cliente MAPI llaman a la función MAPILogonEx para iniciar sesión en una sesión con el sistema de mensajería. Todas las cadenas que se pasan en y son devueltas a y desde las llamadas MAPI están terminada en null y deben especificarse en el juego de caracteres actual o de código de página del sistema operativo cliente o del proveedor de llamada.
  
Si hay una sesión anterior existente que se llama a MapiLogonEx con el conjunto de marca MAPI_ALLOW_OTHERS y si la marca MAPI_NEW_SESSION no está establecida, se omite el parámetro _lpszProfileName_ . Si el parámetro _lpszProfileName_ es NULL o apunta a una cadena vacía y el parámetro _flFlags_ incluye el indicador MAPI_LOGON_UI, la función MAPILogonEx genera un cuadro de diálogo de inicio de sesión que tiene un campo vacío para el nombre del perfil. 
  
Al iniciar sesión en un perfil específico, un cliente debe pasar la marca MAPI_NEW_SESSION a MAPILogonEx además del nombre de perfil. De lo contrario, si otro cliente ha establecido una sesión compartida por inicio de sesión con MAPI_ALLOW_OTHERS, el cliente se registrará a la sesión compartida en lugar de hacerlo en el perfil solicitada. 
  
El indicador MAPI_EXPLICIT_PROFILE no hace que el nombre de perfil predeterminado que se utilizará cuando _lpszProfileName_ es NULL o vacío a menos que el indicador MAPI_USE_DEFAULT también está presente. 
  
El indicador MAPI_NO_MAIL tiene varios efectos que hacen lo siguiente cuando no se utiliza a la cola MAPI:
  
- Puede enviar ningún mensaje o emitido por la cola MAPI durante esta sesión. Sólo los proveedores de almacén y transporte acoplados pueden enviar y entregar mensajes. 
    
- Almacenes en función de servidor aún es posible que enviar o entregar los mensajes. 
    
- No se procesan los mensajes enviados o entregados por almacenes en función de servidor por todos los proveedores de enlace. 
    
- Opciones de cada mensaje y por destinatario para los transportes no están disponibles. 
    
- La tabla de estado no contiene entradas para los proveedores de transporte y cualquier funcionalidad de transporte dependientes en objetos de estado (por ejemplo, configuración) no está disponible. 
    
- La fila de la cola de mensajes en la tabla de estado contiene el valor STATUS_FAILURE. 
    
- Se permiten los inicios de sesión superpuestos, pero los inicios de sesión no hacen que el inicio de sesión anterior recibir actualizaciones de objeto de estado. 
    
Un servicio siempre debe iniciar sesión con la marca MAPI_NO_MAIL. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::MAPILogonEx  <br/> |MFCMAPI usa el método MAPILogonEx para iniciar sesión en MAPI.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

