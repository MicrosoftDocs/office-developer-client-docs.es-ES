---
title: Creación de un perfil mediante el uso de código personalizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 74869293215b86c69ab4e0b1337be6014419fa3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816619"
---
# <a name="creating-a-profile-by-using-custom-code"></a>Creación de un perfil mediante el uso de código personalizado

  
  
**Se aplica a**: Outlook 
  
Si opta por escribir código para crear un perfil, asegúrese de que comprende cómo ordenar las entradas del perfil y el tipo y la cantidad de información que se necesita para cada entrada. Las implicaciones de las entradas de ordenación en un perfil se explica en [Perfiles de MAPI](mapi-profiles.md).
  
 **Para crear un perfil con el código de C o C++**
  
1. Leer el archivo de encabezado para cada servicio de mensajes. Comprender qué propiedades debe configurar y qué valores se va a usar.
    
2. Llame a la función [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de interfaz **IProfAdmin** . 
    
3. Llame a [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) para crear un perfil. Si desea crear un perfil con los servicios de mensaje que aparecen en la sección **[Services predeterminado]** de la MAPISVC. Archivo INF, establecer la marca MAPI_DEFAULT_SERVICE. Si desea habilitar al usuario para escribir información de configuración, establecer la marca MAPI_DIALOG. Asegúrese de que se establezca esta marca si no está disponible a través de la MAPISVC toda la información necesaria. Archivo INF. **CreateProfile** llama a la función de punto de entrada para cada servicio de mensajes que se agregará al perfil con MSG_SERVICE_CREATE establecido como el parámetro _ulContext_ . 
    
4. Llame a [IProfAdmin::AdminServices](iprofadmin-adminservices.md) para obtener un objeto de administración del servicio de mensajes. 
    
5. Use el objeto de administración del servicio de mensajes para agregar servicios de mensajes para el perfil. Para cada servicio de mensajes que desea agregar:
    
1. Llame al método [IMsgServiceAdmin::](imsgserviceadmin-createmsgservice.md) para crear el nuevo servicio de mensaje. 
    
2. Llame a [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), pasando la estructura **MAPIUID** del servicio que acaba de crear y una matriz de valores de propiedad con sus propiedades de configuración. 
    
6. Para recuperar el identificador de un servicio recién agregado, que es su propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), llame a [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obtener acceso a la tabla de mensajes de servicio y la búsqueda de la fila que representa el servicio de mensajes. La última fila de la tabla representa el servicio de mensajes agregado más recientemente. 
    
Para hacer que un nuevo perfil temporal, llame al método [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) inmediatamente después de iniciar sesión. **DeleteProfile** marcará el nuevo perfil como eliminada mientras realiza utilizable para la duración de la sesión. Debido a que no se incluirá en la tabla de perfiles de la sesión, otros clientes podrán utilizarlo. 
  

