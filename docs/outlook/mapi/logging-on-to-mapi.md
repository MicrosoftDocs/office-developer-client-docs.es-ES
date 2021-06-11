---
title: Iniciar sesión en MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 05bafe43-a78a-4659-92f0-0b4fe444c64f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cce43301ac73a5646e263b2ab92700e57804637d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419712"
---
# <a name="logging-on-to-mapi"></a>Iniciar sesión en MAPI
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente inician sesión en el subsistema MAPI llamando a la **función MAPILogonEx.** Para obtener más información, vea [MAPILogonEx](mapilogonex.md). **MAPILogonEx valida** la selección de perfiles y la configuración de cada proveedor de servicios en el perfil. Una vez configurado, MAPI inicia los proveedores de libreta de direcciones antes de iniciar los proveedores de almacén de mensajes. Los proveedores de transporte se inician cuando sus servicios son necesarios por primera vez. 
  
## <a name="choose-a-profile"></a>Elegir un perfil
  
- Pase una cadena de caracteres que represente el nombre del perfil en el parámetro  _lpszProfileName_ a **MAPILogonEx** o...
    
- Permitir al usuario especificar el perfil pasando NULL en el parámetro  _lpszProfileName_ y estableciendo la marca MAPI_LOGON_UI, o... 

- Seleccione el perfil predeterminado pasando NULL en el  _parámetro lpszProfileName_ y estableciendo MAPI_USE_DEFAULT marca. 
    
Si necesita un perfil específico que no sea el perfil predeterminado, debe guardar su nombre en su propia base de datos de configuración o usar una convención de nomenclatura específica. MAPI no expone ningún atributo de perfil que no sea el nombre y la marca predeterminada en la tabla de perfiles, y la marca de perfil predeterminada está reservada para aplicaciones IPM relacionadas y cliente de mensajería.
  
Los clientes que proporcionen información de configuración parcial de perfil o proveedor a **MAPILogonEx** deben solicitar al usuario los datos adicionales al permitir que se muestre un cuadro de diálogo. Si falta información y **MAPILogonEx** no puede pedir al usuario que la proporcione, se produce un error en el inicio de sesión. Los clientes que no necesitan la entrada del usuario pueden suprimir la presentación del cuadro de diálogo. 
  
Las marcas que **MAPILogonEx** usa para habilitar una interfaz de usuario son mutuamente excluyentes; solo se puede establecer uno. Dejar estas marcas sin establecer suprime la presentación de una interfaz de usuario, lo que hace que **MAPILogonEx** falle si falta información necesaria. Es decir, si deshabilita la interfaz de usuario y pasa NULL para el parámetro  _lpszProfileName_ y no establece la marca MAPI_USE_DEFAULT, **MAPILogonEx** producirá un error porque no puede recuperar un nombre de perfil. 
  
La sesión que **MAPILogonEx** establece puede ser una sesión de mensajería individual, una sesión de mensajería compartida o una sesión de no meseo. Las sesiones de mensajería individuales son conexiones privadas entre el cliente y el subsistema MAPI y se pueden establecer estableciendo la marca MAPI_NEW_SESSION en la llamada a **MAPILogonEx**.
  
Las sesiones de mensajería compartida son conexiones que pueden usar varios clientes de mensajería. Normalmente, las sesiones compartidas se establecen para que los clientes usen el mismo perfil. Para establecer una nueva sesión como sesión compartida, establezca la marca MAPI_ALLOW_OTHERS sesión. 
  
## <a name="use-an-existing-shared-session"></a>Usar una sesión compartida existente
  
- No establezca la marca MAPI_NEW_SESSION.
    
- No establezca la marca MAPI_ALLOW_OTHERS.
    
- Pase NULL para el _parámetro lpszProfileName._ 
    
- Pase NULL para el _parámetro lpszPassword._ 
    
Las sesiones que no son de almacenamiento permiten a los clientes tener acceso al subsistema MAPI, pero no permiten que los mensajes se envíen o reciban. Las aplicaciones de configuración o administración son ejemplos de clientes que pueden necesitar establecer sesiones que no sean de uso. Para solicitar una sesión que no es demesaje, establezca MAPI_NO_MAIL marca. Al establecer esta marca, el cliente inicia sesión sin informar a la cola MAPI. Los clientes que inician sesión en MAPI con esta marca no pueden esperar recibir informes de estado de lectura.
  
La MAPI_NO_MAIL solo debe establecerse:
  
- Si el cliente no enviará ni recibirá mensajes durante la sesión.
    
- Si el cliente tiene un control total sobre el contenido del perfil y los mensajes se envían y reciben mediante proveedores de transporte y almacén de mensajes estrechamente acoplados, como los proveedores de Exchange Microsoft.
    
Un cliente de mensajería puede compartir una sesión con un cliente que no está en uso. Las características de un miembro de una sesión compartida no se ven afectadas por las características de otros miembros. Es decir, si inicia sesión con las marcas MAPI_NO_MAIL y MAPI_ALLOW_OTHERS establecidas, un cliente de mensajería que inicie sesión en la sesión no afectará al funcionamiento del cliente y viceversa. El cliente de mensajería seguirá siendo capaz de enviar y recibir mensajes y el cliente no lo hará.
  
**MAPILogonEx** define algunas otras marcas que puede establecer: 
  
- MAPI_FORCE_DOWNLOAD indica que los mensajes entrantes deben descargarse antes de **que MAPILogonEx devuelva.** Si no se establece esta marca, los mensajes se descargarán en segundo plano más adelante. 
    
- MAPI_SERVICE_UI_ALWAYS solicita que todos los servicios de mensajes del perfil muestren un cuadro de diálogo de configuración.
    
- MAPI_NT_SERVICE indica que el cliente se implementa como un servicio Windows cliente. Esta marca debe establecerse si el cliente es un servicio.
    
Con cada inicio de sesión correcto, **MAPILogonEx** devuelve un puntero a una sesión MAPI. Puede usar este puntero para llamar a los métodos de la **interfaz IMAPISession.** Para obtener más información, [vea IMAPISession : IUnknown](imapisessioniunknown.md). Los punteros de sesión, independientemente del tipo de sesión, son únicos para los clientes que los reciben y no son válidos en todas las tareas.
  

