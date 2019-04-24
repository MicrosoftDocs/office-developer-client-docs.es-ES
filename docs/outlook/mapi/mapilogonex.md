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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346651"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra una aplicación cliente en una sesión con el sistema de mensajería. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix. h  <br/> |
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
  
> a Identificador de la ventana a la que el cuadro de diálogo de inicio de sesión es modal. Si no aparece ningún cuadro de diálogo durante la llamada, se omite el parámetro _ulUIParam_ . Este parámetro puede ser cero. 
    
 _lpszProfileName_
  
> a Puntero a una cadena que contiene el nombre del perfil que se usará cuando el usuario inicie sesión. Esta cadena está limitada a 64 caracteres.
    
 _lpszPassword_
  
> a Puntero a una cadena que contiene la contraseña del perfil. El parámetro _lpszPassword_ debe ser null. 
    
 _flFlags_
  
> a Máscara de la máscara usada para controlar cómo se realiza el inicio de sesión. Se pueden establecer los siguientes indicadores:
    
MAPI_ALLOW_OTHERS 
  
> La sesión compartida debe devolverse, lo que permite a los clientes posteriores obtener la sesión sin especificar credenciales de usuario. 
    
MAPI_BG_SESSION
  
> Inicie sesión en una sesión y ejecute las operaciones en segundo plano. En general, si un cliente intenta realizar el procesamiento en un subproceso en segundo plano o en un proceso independiente de una manera que no molesta al subproceso en primer plano, debe llamar con la marca MAPI_BG_SESSION. Una aplicación cliente como un motor de indización o abrir un archivo de carpetas personales (PST) para el acceso de tipo en segundo plano son algunos ejemplos de dónde usar MAPI_BG_SESSION. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> El perfil predeterminado no debe usarse y el usuario debe ser necesario para proporcionar un perfil. 
    
MAPI_EXTENDED 
  
> Inicie sesión con capacidades extendidas. Este indicador debe establecerse siempre.
    
MAPI_FORCE_DOWNLOAD 
  
> Debe intentar descargar todos los mensajes del usuario antes de volver. Si no se establece la marca MAPI_FORCE_DOWNLOAD, los mensajes se pueden descargar en segundo plano después de que se devuelva la llamada a MAPILogonEx. 
    
MAPI_LOGON_UI 
  
> Se debe mostrar un cuadro de diálogo para pedir al usuario la información de inicio de sesión si es necesario. Si no se establece la marca MAPI_LOGON_UI, el cliente que realiza la llamada no muestra un cuadro de diálogo de inicio de sesión y devuelve un valor de error si el usuario no ha iniciado sesión.
    
MAPI_NEW_SESSION 
  
> Debe realizarse un intento de crear una nueva sesión MAPI en lugar de adquirir la sesión compartida. Si no se establece la marca MAPI_NEW_SESSION, MAPILogonEx usa una sesión compartida existente incluso si el parámetro _lpszprofileName_ no es NULL. 
    
MAPI_NO_MAIL 
  
> MAPI no debe informar a la cola MAPI de la existencia de la sesión. El resultado es que no se pueden enviar o recibir mensajes en la sesión, excepto a través de un par de almacén y transporte estrechamente acoplados. Un cliente de llamada establece esta marca si actúa como un agente, en caso de que deba realizarse el trabajo de configuración o si el cliente está explorando los almacenes de mensajes disponibles. 
    
MAPI_NT_SERVICE 
  
> El autor de la llamada se está ejecutando como un servicio de Windows. Las personas que llaman que no se ejecutan como un servicio de Windows no deben establecer esta marca; los autores de llamadas que se ejecutan como servicio deben establecer esta marca. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx debe mostrar un cuadro de diálogo de configuración para cada servicio de mensajes en el perfil. Los cuadros de diálogo se muestran después de elegir el perfil, pero antes de que el servicio de mensajes haya iniciado sesión. El cuadro de diálogo común de MAPI para inicio de sesión también contiene una casilla de verificación que solicita la misma operación. 
    
MAPI_TIMEOUT_SHORT 
  
> El inicio de sesión debe fallar si se bloquea durante más de unos pocos segundos. 
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI. 
    
MAPI_USE_DEFAULT 
  
> El subsistema de mensajería debe sustituir el nombre de perfil del perfil predeterminado por el parámetro _lpszProfileName_ . La marca MAPI_EXPLICIT_PROFILE se omite a menos que _lpszProfileName_ sea NULL o esté vacío. 
    
 _lppSession_
  
> contempla Puntero a un puntero a la interfaz de sesión MAPI.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El inicio de sesión se realizó correctamente.
    
MAPI_E_LOGON_FAILED 
  
> El inicio de sesión no se pudo realizar correctamente, ya sea porque uno o varios de los parámetros de MAPILogonEx no eran válidos o porque había demasiadas sesiones abiertas todavía.
    
MAPI_E_TIMEOUT 
  
> MAPI serializa todos los inicios de sesión a través de una exclusión mutua. Se devuelve si se estableció la marca MAPI_TIMEOUT_SHORT y otro subproceso contenía la exclusión mutua. 
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Las aplicaciones de cliente MAPI llaman a la función MAPILogonEx para iniciar sesión en una sesión con el sistema de mensajería. Todas las cadenas que se pasan y se devuelven y desde llamadas MAPI se terminan en NULL y deben especificarse en el juego de caracteres actual o la página de códigos del sistema operativo del proveedor o del cliente que realiza la llamada.
  
El parámetro _lpszProfileName_ se omite si hay una sesión anterior existente que llama a MapiLogonEx con el valor de la marca MAPI_ALLOW_OTHERS establecida y si no se ha establecido el indicador MAPI_NEW_SESSION. Si el parámetro _lpszProfileName_ es null o apunta a una cadena vacía y el parámetro _flFlags_ incluye la marca MAPI_LOGON_UI, la función MAPILogonEx genera un cuadro de diálogo de inicio de sesión que tiene un campo vacío para el nombre del perfil. 
  
Al iniciar sesión en un perfil específico, un cliente debe pasar la marca MAPI_NEW_SESSION a MAPILogonEx, además del nombre del perfil. De lo contrario, si otro cliente ha establecido una sesión compartida mediante el inicio de sesión con MAPI_ALLOW_OTHERS, el cliente se conectará a la sesión compartida en lugar del perfil solicitado. 
  
La marca MAPI_EXPLICIT_PROFILE no hace que se use el nombre de perfil predeterminado cuando _lpszProfileName_ es null o está vacío, a menos que la marca MAPI_USE_DEFAULT también esté presente. 
  
La marca MAPI_NO_MAIL tiene varios efectos que provocan lo siguiente cuando no se usa la cola MAPI:
  
- La cola MAPI no puede enviar ni entregar mensajes durante esta sesión. Solo los proveedores de almacenamiento y transporte estrechamente acoplados pueden enviar y entregar mensajes. 
    
- Los almacenes basados en el servidor podrían seguir enviando o entregando mensajes. 
    
- Los proveedores de enlaces no procesan los mensajes enviados o entregados por los almacenes basados en el servidor. 
    
- Las opciones por mensaje y por destinatario para los transportes no están disponibles. 
    
- La tabla de estado no contiene entradas para los proveedores de transporte y la funcionalidad de transporte que dependa de los objetos de estado (como la configuración) no está disponible. 
    
- La fila de cola de mensajes de la tabla de estado contiene el valor STATUS_FAILURE. 
    
- Se permiten los inicios de sesión superpuestos, pero dichos inicios de sesión no causan que el inicio de sesión anterior Reciba actualizaciones de objetos de estado. 
    
Un servicio siempre debe iniciar sesión con la marca MAPI_NO_MAIL. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIObjects. cpp  <br/> |CMapiObjects:: MAPILogonEx  <br/> |MFCMAPI usa el método MAPILogonEx para iniciar sesión en MAPI.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

