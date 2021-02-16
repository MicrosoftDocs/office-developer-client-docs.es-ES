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
  
Las aplicaciones cliente inician sesión en el subsistema MAPI llamando a la **función MAPILogonEx.** Para obtener más información, vea [MAPILogonEx](mapilogonex.md). **MAPILogonEx valida** la selección de perfil y la configuración de cada proveedor de servicios en el perfil. Una vez configurado, MAPI inicia los proveedores de libretas de direcciones antes de iniciar los proveedores de almacén de mensajes. Los proveedores de transporte se inician cuando sus servicios son necesarios por primera vez. 
  
## <a name="choose-a-profile"></a>Elegir un perfil
  
- Pase una cadena de caracteres que represente el nombre del perfil en el parámetro  _lpszProfileName_ a **MAPILogonEx** o...
    
- Permitir que el usuario especifique el perfil pasando NULL en el parámetro  _lpszProfileName_ y estableciendo el MAPI_LOGON_UI marca, o... 

- Seleccione el perfil predeterminado pasando NULL en el  _parámetro lpszProfileName_ y estableciendo la MAPI_USE_DEFAULT predeterminada. 
    
Si necesita un perfil específico que no sea el predeterminado, debe guardar su nombre en su propia base de datos de configuración o usar una convención de nomenclatura específica. MAPI no expone ningún atributo de perfil que no sea el nombre y la marca predeterminada en la tabla de perfil, y el indicador de perfil predeterminado está reservado para el cliente de mensajería y las aplicaciones IPM relacionadas.
  
Los clientes que suministran información de configuración parcial de perfiles o proveedores a **MAPILogonEx** deben solicitar al usuario los datos adicionales al permitir que se muestre un cuadro de diálogo. Si falta información y **MAPILogonEx** no puede pedir al usuario que la proporcione, se produce un error en el inicio de sesión. Los clientes que no necesitan la entrada del usuario pueden suprimir la presentación del cuadro de diálogo. 
  
Las marcas que **MAPILogonEx** usa para habilitar una interfaz de usuario son mutuamente excluyentes; solo se puede establecer uno. Si deja estas marcas sin establecer, se suprime la presentación de una interfaz de usuario, lo que provoca un error en **MAPILogonEx** si falta información necesaria. Es decir, si deshabilita la interfaz de usuario y pasa NULL para el parámetro  _lpszProfileName_ y no establece la marca MAPI_USE_DEFAULT, **MAPILogonEx** producirá un error porque no puede recuperar un nombre de perfil. 
  
La sesión que **establece MAPILogonEx** puede ser una sesión de mensajería individual, una sesión de mensajería compartida o una sesión que no está en uso. Las sesiones de mensajería individuales son conexiones privadas entre el cliente y el subsistema MAPI y se pueden establecer estableciendo la marca MAPI_NEW_SESSION en la llamada a **MAPILogonEx**.
  
Las sesiones de mensajería compartidas son conexiones que pueden usar varios clientes de mensajería. Las sesiones compartidas suelen establecerse para que los clientes usen el mismo perfil. Para establecer una nueva sesión como sesión compartida, establezca la marca MAPI_ALLOW_OTHERS sesión. 
  
## <a name="use-an-existing-shared-session"></a>Usar una sesión compartida existente
  
- No establezca la marca MAPI_NEW_SESSION página.
    
- No establezca la marca MAPI_ALLOW_OTHERS página.
    
- Pase NULL para el _parámetro lpszProfileName._ 
    
- Pase NULL para el _parámetro lpszPassword._ 
    
Las sesiones que no son de almacenamiento permiten a los clientes tener acceso al subsistema MAPI, pero no permiten que se envíen o reciban mensajes. Las aplicaciones de configuración o administración son ejemplos de clientes que pueden necesitar establecer sesiones nomesaging. Para solicitar una sesión que no se mime, establezca la marca MAPI_NO_MAIL cliente. Al establecer esta marca, se inicia la sesión del cliente sin informar a la cola MAPI. Los clientes que inician sesión en MAPI con esta marca no pueden esperar recibir informes de estado de lectura.
  
La MAPI_NO_MAIL solo debe establecerse:
  
- Si el cliente no enviará ni recibirá mensajes durante la sesión.
    
- Si el cliente tiene control total sobre el contenido del perfil y los mensajes se envían y reciben usando proveedores de transporte y almacén de mensajes estrechamente acoplados, como los proveedores de Microsoft Exchange.
    
Un cliente de mensajería puede compartir una sesión con un cliente que no está en uso. Las características de un miembro de una sesión compartida no se ven afectadas por las características de otros miembros. Es decir, si inicia sesión con las marcas MAPI_NO_MAIL y MAPI_ALLOW_OTHERS establecidas, el inicio de sesión de un cliente de mensajería en la sesión no afecta al funcionamiento del cliente y viceversa. El cliente de mensajería seguirá siendo capaz de enviar y recibir mensajes y el cliente no lo podrá hacer.
  
**MAPILogonEx** define algunas otras marcas que puede establecer: 
  
- MAPI_FORCE_DOWNLOAD indica que los mensajes entrantes deben descargarse antes de **que mapiLogonEx** vuelva. Si no se establece esta marca, los mensajes se descargarán en segundo plano más adelante. 
    
- MAPI_SERVICE_UI_ALWAYS solicita que todos los servicios de mensajes del perfil muestren un cuadro de diálogo de configuración.
    
- MAPI_NT_SERVICE indica que el cliente está implementado como un servicio de Windows. Esta marca debe establecerse si el cliente es un servicio.
    
Con cada inicio de sesión correcto, **MAPILogonEx** devuelve un puntero a una sesión MAPI. Puede usar este puntero para llamar a los métodos de la **interfaz IMAPISession.** Para obtener más información, [vea IMAPISession : IUnknown](imapisessioniunknown.md). Los punteros de sesión, independientemente del tipo de sesión, son únicos para los clientes que los reciben y no son válidos en todas las tareas.
  

