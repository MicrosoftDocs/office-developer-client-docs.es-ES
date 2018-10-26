---
title: Sesiones de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c5a7c137-393e-40ff-a2b9-afe02da2435a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a2ab44081c79e72e082687006ab06d0f83b8367e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575031"
---
# <a name="mapi-sessions"></a>Sesiones de MAPI

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Antes de la aplicaci�n cliente puede llamar a un sistema de mensajer�a subyacente, debe establecer una conexi�n con el subsistema MAPI o sesi�n.
  
Sessions are initiated when a user logs on, a process that accesses a valid profile and validates the messaging system and the message service credentials. Then, the process ensures that all of the profile's message services are correctly configured. The client interface you use determines the logon call. MAPI clients call the [MAPILogonEx](mapilogonex.md) function. 
  
Configuraci�n del servicio de mensajes es uno de los elementos m�s importantes del proceso de inicio de sesi�n. El perfil es el origen para la informaci�n de configuraci�n. Si falta informaci�n de un servicio de mensaje en particular, el proceso de inicio de sesi�n intenta pedir al usuario que suministrar. No siempre es correcta por dos motivos: en primer lugar, preguntar al usuario requiere la presentaci�n de un cuadro de di�logo. Es posible que los clientes no permitir la presentaci�n de una interfaz de usuario pasando una marca a la llamada de inicio de sesi�n. En segundo lugar, el usuario puede cancelar el cuadro de di�logo antes de poder agregar la informaci�n necesaria.
  
Cuando un proceso de inicio de sesi�n falla una vez, el usuario est� informado del error y se le ofrece la posibilidad de volver a intentar o corregir la condici�n de error. Una vez m�s, una interfaz de usuario se mostrar�, si permite que el cliente y el usuario le pedir� que especifique los datos que sean que faltan. Si este segundo intento se realiza correctamente, MAPI deshabilita a todos los proveedores de servicio en el servicio de mensajes para la duraci�n de la sesi�n. En efecto, se deshabilita el servicio de mensaje entero. Esto significa que ninguno de los proveedores de servicios en el servicio de mensajes pueden trabajar. Esto se hace porque si un proveedor se produce un error de inicio de sesi�n, los dem�s proveedores normalmente tambi�n producir� un error. El proceso de inicio de sesi�n puede producirse un error debido a una ruta de acceso no v�lida para un recurso es necesario, una versi�n incompatible de MAPI, un servidor de mensajer�a no disponible o da�os en los datos. 
  
Los clientes pueden especificar uno de los dos tipos de sesiones establecerse en la llamada de inicio de sesi�n: una sesi�n individual o una sesi�n compartida. Sesiones individuales son conexiones privadas; hay una relaci�n uno a uno entre una aplicaci�n cliente y la sesi�n que est� usando. Como consecuencia, las aplicaciones de cliente que comparten una sesi�n tambi�n compartan un perfil. Sesiones compartidas se establecen una vez, pero pueden usar otras aplicaciones cliente que necesitan usarlos. El perfil y las credenciales se especifican s�lo con el inicio de sesi�n inicial. 
  
Los clientes pueden iniciar sesi�n varias veces como el mismo usuario o varios usuarios. MAPI no evitarlo. Algunos proveedores de servicios, sin embargo, podr�an no ser tan flexibles, devuelve el valor de error MAPI_E_SESSION_LIMIT en los intentos de inicio de sesi�n subsiguientes. Proveedores de servicios con limitaciones de hardware subyacentes pueden necesitar para aplicar un l�mite de sesi�n.
  
Las llamadas de funci�n para establecer una sesi�n tienen una colecci�n de par�metros y los indicadores que controlan c�mo se crea la sesi�n. El cliente especifica un nombre de perfil opcional y un identificador de ventana que act�a como la ventana principal de los cuadros de di�logo que se muestran. Las marcas son MAPI_NEW_SESSION, que solicita que se puede establecer una sesi�n nueva, individual (en lugar de una sesi�n compartida), y el indicador de interfaz de usuario MAPI_LOGON_UI. El indicador de la interfaz de usuario se establece para solicitar un cuadro de di�logo de inicio de sesi�n.
  
En la siguiente ilustraci�n muestra c�mo estos diversos par�metros y marcas de establecen una sesi�n MAPI.
  
**Diagrama de flujo de sesi�n de MAPI**
  
![Diagrama de flujo de sesión MAPI] (media/amapi_47.gif "Diagrama de flujo de sesión MAPI")
  
For information about handling sessions from within a client application, see [Control de sesi�n MAPI](mapi-session-handling.md)
  
## <a name="see-also"></a>Vea tambi�n

- [MAPILogonEx](mapilogonex.md)  
- [IMAPISession: IUnknown](imapisessioniunknown.md)
- [Control de sesi�n MAPI](mapi-session-handling.md)  
- [Informaci�n general sobre programaci�n de MAPI](mapi-programming-overview.md)

