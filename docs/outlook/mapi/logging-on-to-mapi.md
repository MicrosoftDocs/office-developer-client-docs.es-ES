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
ms.openlocfilehash: 1ae3c47964ff238f57e98e0005a966008192f7c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818050"
---
# <a name="logging-on-to-mapi"></a>Iniciar sesión en MAPI
 
**Hace referencia a**: Outlook 
  
Las aplicaciones cliente inicie sesión en el subsistema MAPI mediante una llamada a la función **MAPILogonEx** . Para obtener más información, vea [MAPILogonEx](mapilogonex.md). **MAPILogonEx** valida la selección de perfiles y la configuración de cada proveedor de servicios en el perfil. Una vez configurado, MAPI inicia los proveedores de la libreta de direcciones antes de iniciar los proveedores de almacén de mensajes. Los proveedores de transporte se han iniciado cuando primero se requieren sus servicios. 
  
## <a name="choose-a-profile"></a>Elija un perfil
  
- Pase una cadena de caracteres que representa el nombre del perfil en el parámetro _lpszProfileName_ a **MAPILogonEx**, o...
    
- Permitir que el usuario especificar el perfil pasando NULL en el parámetro _lpszProfileName_ y estableciendo el indicador MAPI_LOGON_UI, o... 

- Seleccione el perfil predeterminado pasando NULL en el parámetro _lpszProfileName_ y establecer el indicador MAPI_USE_DEFAULT. 
    
Si necesita un perfil específico que no sea el perfil predeterminado, debe guardar su nombre en su propia base de datos de configuración o utilizar una convención de nomenclatura específica. MAPI no expone los atributos de perfil que no sean de la marca de nombre y un valor predeterminado en la tabla de perfil y el indicador de perfil predeterminado está reservado para la mensajería de cliente y las aplicaciones de IPM relacionadas.
  
Los clientes que proporcionan perfil parcial o información de configuración de proveedor a **MAPILogonEx** deben preguntar al usuario para los datos adicionales al permitir que se muestre un cuadro de diálogo. Si falta información y **MAPILogonEx** no se puede pedir al usuario que proporcionarla, se produce un error en el inicio de sesión. Los clientes que realizan la entrada del usuario necesidad no pueden suprimir la visualización de cuadro de diálogo. 
  
Los indicadores que **MAPILogonEx** se usa para habilitar una interfaz de usuario son mutuamente excluyentes; se puede establecer sólo uno. Salir sin establecer estos marcadores, suprime la visualización de una interfaz de usuario, lo que provoca que **MAPILogonEx** provocarán un error si falta información necesaria. Es decir, si deshabilita la interfaz de usuario y pase NULL para el parámetro _lpszProfileName_ y no se establece la marca MAPI_USE_DEFAULT, se producirá un error en **MAPILogonEx** porque no se puede recuperar un nombre de perfil. 
  
La sesión que establece la **MAPILogonEx** puede ser una sesión de mensajería individual, una sesión de mensajería compartida o una sesión de nonmessaging. Sesiones de mensajería individuales son conexiones privadas entre el cliente y el subsistema MAPI y pueden establecerse mediante la configuración de la marca MAPI_NEW_SESSION en la llamada a **MAPILogonEx**.
  
Sesiones de mensajería compartidas son las conexiones que pueden usar varios clientes de mensajería. Normalmente, se establecen las sesiones compartidas para los clientes usan el mismo perfil. Para establecer una sesión de nuevo como una sesión compartida, establecer la marca MAPI_ALLOW_OTHERS. 
  
## <a name="use-an-existing-shared-session"></a>Usar una sesión compartida existente
  
- No se establece la marca MAPI_NEW_SESSION.
    
- No se establece la marca MAPI_ALLOW_OTHERS.
    
- Pase NULL para el parámetro _lpszProfileName_ . 
    
- Pase NULL para el parámetro _lpszPassword_ . 
    
Sesiones nonmessaging permitir que los clientes tener acceso el subsistema MAPI, pero no permitir los mensajes ser enviados o recibidos. Configuración o administración de aplicaciones son ejemplos de clientes que es posible que deba establecer sesiones nonmessaging. Para solicitar una sesión de nonmessaging, establecer la marca MAPI_NO_MAIL. Al establecer este indicador los registros de su cliente sin informar a la cola de MAPI. Los clientes que inicie sesión en MAPI con esta marca no puede esperar que nunca recibirá informes de estado de lectura.
  
Sólo se debe establecer la marca MAPI_NO_MAIL:
  
- Si el cliente no va a enviar o recibir mensajes durante la sesión.
    
- Si su cliente tiene control total sobre el contenido del perfil y los mensajes se envían y reciben mediante acoplado almacén de mensajes y los proveedores, como los proveedores de Microsoft Exchange de transporte.
    
Un cliente de mensajería puede compartir una sesión con un cliente nonmessaging. Las características de un miembro de una sesión compartida no se ven afectadas por las características de otros miembros. Es decir, si se inicia sesión con el conjunto de indicadores MAPI_NO_MAIL y MAPI_ALLOW_OTHERS, un cliente de mensajería de inicio de sesión para la sesión no tiene efecto en la operación de su cliente y viceversa. El cliente de mensajería aún podrá enviar y recibir mensajes y no el cliente.
  
**MAPILogonEx** define unos otros marcadores que puede establecer: 
  
- MAPI_FORCE_DOWNLOAD indica que los mensajes entrantes que deben descargarse antes de **MAPILogonEx** devuelve. Si no se establece este indicador hace que los mensajes se descargan en segundo plano en un momento posterior. 
    
- MAPI_SERVICE_UI_ALWAYS solicita que cada servicio de mensajes en el perfil de mostrar un cuadro de diálogo de configuración.
    
- MAPI_NT_SERVICE indica que el cliente se implementa como un servicio de Windows. Si el cliente es un servicio, se debe establecer este indicador.
    
Con cada inicio de sesión correcto, **MAPILogonEx** devuelve un puntero a una sesión de MAPI. Puede usar este puntero para llamar a los métodos de la interfaz **IMAPISession** . Para obtener más información, vea [IMAPISession: IUnknown](imapisessioniunknown.md). Punteros de sesión, independientemente del tipo de sesión, son exclusivos de los clientes que reciben y no son válidos a través de tareas.
  

