---
title: Creación de un perfil mediante código personalizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413307"
---
# <a name="creating-a-profile-by-using-custom-code"></a>Creación de un perfil mediante código personalizado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si decide escribir código para crear un perfil, asegúrese de comprender cómo ordenar entradas de perfil y el tipo y la cantidad de información que se necesita para cada entrada. Las implicaciones de ordenar entradas en un perfil se explican en [Perfiles MAPI](mapi-profiles.md).
  
 **Para crear un perfil con código C o C++**
  
1. Lea el archivo de encabezado de cada servicio de mensajes. Comprenda qué propiedades necesitará configurar y qué valores usará.
    
2. Llame a [la función MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de **interfaz IProfAdmin.** 
    
3. Llama [a IProfAdmin::CreateProfile](iprofadmin-createprofile.md) para crear tu perfil. Si desea crear un perfil con los servicios de mensajes enumerados en la sección **[Servicios predeterminados]** de MAPISVC. INF, establezca la marca MAPI_DEFAULT_SERVICE. Si desea habilitar al usuario para escribir información de configuración, establezca la marca MAPI_DIALOG configuración. Asegúrese de establecer esta marca si no toda la información necesaria está disponible a través de MAPISVC. Archivo INF. **CreateProfile** llama a la función de punto de entrada de cada servicio de mensajes que se agregará al perfil con MSG_SERVICE_CREATE establecer como el _parámetro ulContext._ 
    
4. Llame [a IProfAdmin::AdminServices](iprofadmin-adminservices.md) para obtener un objeto de administración del servicio de mensajes. 
    
5. Use el objeto de administración del servicio de mensajes para agregar servicios de mensajes al perfil. Para cada servicio de mensajes que desee agregar:
    
1. Llame al [método IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) para crear el nuevo servicio de mensajes. 
    
2. Llame [a IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), pasando la estructura **MAPIUID** del servicio que acaba de crear y una matriz de valores de propiedad con sus propiedades de configuración. 
    
6. Para recuperar el identificador de un servicio recién agregado, que es su propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), llame a [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obtener acceso a la tabla de servicio de mensajes y buscar la fila que representa el servicio de mensajes. La última fila de la tabla representará el servicio de mensajes agregado más recientemente. 
    
Para convertir un nuevo perfil en temporal, llama al [método IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md) inmediatamente después de iniciar sesión. **DeleteProfile** marcará el nuevo perfil como eliminado mientras lo hace utilizable durante la duración de la sesión. Dado que no se incluirá en la tabla de perfiles de la sesión, otros clientes no podrán usarlo. 
  

