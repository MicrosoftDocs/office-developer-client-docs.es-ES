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
  
Las aplicaciones cliente inician sesión en el subsistema MAPI mediante una llamada a la función **MAPILogonEx** . Para obtener más información, vea [MAPILogonEx](mapilogonex.md). **MAPILogonEx** valida la selección de perfil y la configuración de cada proveedor de servicios en el perfil. Una vez configurado, MAPI inicia los proveedores de la libreta de direcciones antes de iniciar los proveedores de almacenamiento de mensajes. Los proveedores de transporte se inician cuando sus servicios son los primeros necesarios. 
  
## <a name="choose-a-profile"></a>Elegir un perfil
  
- Pase una cadena de caracteres que represente el nombre del perfil en el parámetro _lpszProfileName_ a **MAPILogonEx**, o...
    
- Permita que el usuario especifique el perfil pasando NULL en el parámetro _lpszProfileName_ y estableciendo la marca MAPI_LOGON_UI o... 

- Seleccione el perfil predeterminado pasando NULL en el parámetro _lpszProfileName_ y estableciendo la marca MAPI_USE_DEFAULT. 
    
Si requiere un perfil específico distinto del perfil predeterminado, debe guardar su nombre en su propia base de datos de configuración o usar una Convención de nomenclatura específica. MAPI no expone ningún atributo de perfil que no sea el nombre y la marca predeterminada en la tabla de perfiles, y la marca de perfil predeterminada está reservada para el cliente de mensajería y las aplicaciones IPM relacionadas.
  
Los clientes que proporcionan información de configuración de proveedor o perfil parcial a **MAPILogonEx** deben solicitar al usuario los datos adicionales al permitir que se muestre un cuadro de diálogo. Si falta información y **MAPILogonEx** no puede solicitar al usuario que la suministre, se producirá un error en el inicio de sesión. Los clientes que no necesitan la entrada del usuario pueden suprimir la presentación del cuadro de diálogo. 
  
Los indicadores que usa **MAPILogonEx** para habilitar una interfaz de usuario se excluyen mutuamente; solo se puede establecer un. Si se dejan estas marcas sin establecer, se suprime la presentación de una interfaz de usuario, lo que provoca un error en **MAPILogonEx** si falta información necesaria. Es decir, si deshabilita la interfaz de usuario y pasa NULL para el parámetro _lpszProfileName_ y no establece la marca MAPI_USE_DEFAULT, se producirá un error en **MAPILogonEx** porque no puede recuperar un nombre de perfil. 
  
La sesión que establece **MAPILogonEx** puede ser una sesión de mensajería individual, una sesión de mensajería compartida o una sesión que no sea de mensajería. Las sesiones de mensajería individuales son conexiones privadas entre el cliente y el subsistema MAPI y se pueden establecer estableciendo la marca MAPI_NEW_SESSION en la llamada a **MAPILogonEx**.
  
Las sesiones de mensajería compartida son conexiones que pueden usar varios clientes de mensajería. Las sesiones comPartidas suelen establecerse para que los clientes usen el mismo perfil. Para establecer una nueva sesión como sesión compartida, establezca la marca MAPI_ALLOW_OTHERS. 
  
## <a name="use-an-existing-shared-session"></a>Usar una sesión compartida existente
  
- No establezca la marca MAPI_NEW_SESSION.
    
- No establezca la marca MAPI_ALLOW_OTHERS.
    
- Pase NULL para el parámetro _lpszProfileName_ . 
    
- Pase NULL para el parámetro _lpszPassword_ . 
    
Las sesiones que no son de mensajería permiten que los clientes tengan acceso al subsistema MAPI, pero no permiten que se envíen o reciban mensajes. Las aplicaciones de configuración o administración son ejemplos de clientes que pueden tener que establecer sesiones que no son de mensajería. Para solicitar una sesión que no es de mensajería, establezca la marca MAPI_NO_MAIL. Al establecer este indicador se registra el cliente en sin informar a la cola MAPI. Los clientes que inicien sesión en MAPI con esta marca no pueden esperar nunca recibir informes de estado de lectura.
  
La marca MAPI_NO_MAIL solo debe establecerse:
  
- Si el cliente no va a enviar ni recibir mensajes durante la sesión.
    
- Si el cliente tiene un control total sobre el contenido del perfil y los mensajes se envían y se reciben mediante proveedores de transporte y almacenamiento de mensajes estrechamente acoplados, como los proveedores de Microsoft Exchange.
    
Un cliente de mensajería puede compartir una sesión con un cliente que no sea de mensajería. Las características de un miembro de una sesión compartida no se ven afectadas por las características de otros miembros. Es decir, si inicia sesión con los indicadores MAPI_NO_MAIL y MAPI_ALLOW_OTHERS, un cliente de mensajería que inicie sesión en la sesión no tendrá ningún efecto en el funcionamiento del cliente y viceversa. El cliente de mensajería podrá seguir enviando y recibiendo mensajes, y el cliente no.
  
**MAPILogonEx** define algunos otros marcadores que puede establecer: 
  
- MAPI_FORCE_DOWNLOAD indica que los mensajes entrantes deben descargarse antes de que **MAPILogonEx** vuelva. Si no se establece esta marca, los mensajes se descargan en segundo plano en un momento posterior. 
    
- MAPI_SERVICE_UI_ALWAYS solicita que cada servicio de mensajes en el perfil muestre un cuadro de diálogo de configuración.
    
- MAPI_NT_SERVICE indica que su cliente se ha implementado como un servicio de Windows. Esta marca debe establecerse si el cliente es un servicio.
    
Con cada inicio de sesión correcto, **MAPILogonEx** devuelve un puntero a una sesión MAPI. Puede utilizar este puntero para llamar a los métodos de la interfaz **IMAPISession** . Para obtener más información, vea [IMAPISession: IUnknown](imapisessioniunknown.md). Los punteros de sesión, independientemente del tipo de sesión, son únicos para los clientes que los reciben y no son válidos en todas las tareas.
  

