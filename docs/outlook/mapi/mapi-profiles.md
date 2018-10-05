---
title: Perfiles de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 493c87a4-317d-47ec-850b-342cac59594b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9db1f8e163e44a44df1e798cebccb3639325275e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391433"
---
# <a name="mapi-profiles"></a>Perfiles de MAPI

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Un perfil de almacena información acerca de los proveedores de servicios y los servicios de mensaje que se instalan en un equipo. Para cada sesión, un cliente en tiempo de inicio de sesión selecciona un perfil que describe los servicios y los proveedores que se va a utilizar. Puede elegir entre una colección de los perfiles de un cliente y, si así lo desea, establecer uno como el valor predeterminado. El perfil predeterminado es el perfil que se selecciona automáticamente cuando un cliente inicia una sesión y no ha especificado explícitamente un perfil.
  
También en estos temas, encontrará una explicación de la caché de alias, que se almacena en una secuencia binaria.
  
- [Caché de sobrenombre](nickname-cache.md)
    
- [Secuencia de Autocompletar](autocomplete-stream.md)
    
- [Análisis de archivos binarios](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Secciones del perfil

Los perfiles se dividen en las secciones que los clientes y proveedores de servicios de acceso para mostrar las propiedades de perfil a los usuarios o para realizar cambios de configuración. Una sección de perfil es un objeto MAPI que implementa la interfaz **IProfSect** , una interfaz que se deriva de **IMAPIProp** y no tiene ningún método adicional. Para obtener más información, vea [IProfSect: IMAPIProp](iprofsectimapiprop.md). Su único propósito es manipular las propiedades de una sección de perfil. Para recuperar un puntero **IProfSect** a una sección de perfil determinada, clientes y proveedores de servicios de llamar a los métodos siguientes. 
  
|||
|:-----|:-----|
|Pueden llamar a los clientes:  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Pueden llamar a los proveedores de servicios:  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Pueden llamar a los clientes o proveedores:  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Los perfiles se organizan jerárquicamente mucho al igual que el archivo MAPISVC. Archivo INF. En la parte superior de la jerarquía, hay secciones de perfil que contienen información relevante para el perfil. El nivel intermedio incluye secciones que contienen información acerca de un servicio de mensaje concreto y el nivel inferior incluye secciones que contienen información acerca de uno de los proveedores de servicios en un servicio de mensajes. 
  
Cada perfil tiene varias propiedades necesarias que se almacenan en una o varias de las secciones del perfil. Por ejemplo, cada perfil tiene las propiedades de **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) y **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)). Clave de búsqueda de un perfil se establece en el valor que se define en MAPIGUID. H como MUID_PROFILE_INSTANCE y siempre se garantiza que es único entre todos los perfiles. Aunque dos perfiles pueden tener el mismo nombre, no pueden tener la misma clave de búsqueda. Las claves de búsqueda deben tratarse como datos binarios en lugar de datos de ningún tipo concreto.
  
Los proveedores de almacén de mensajes se requieren para incluir propiedad de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de su almacén de mensajes en las secciones de perfil para el perfil y proveedor de almacén para su mensaje y mantener estas entradas sincronizadas. Cuando se crea un almacén de mensajes, el proveedor establece **PR_DISPLAY_NAME** según el valor almacenado en estas secciones del perfil. 
  
Hay dos diferencias principales entre las secciones de perfil y otros objetos que heredan de **IMAPIProp**: 
  
- Las secciones del perfil no admiten transacciones.
    
- Las secciones del perfil no admiten las propiedades con nombre, devolver MAPI_E_NO_SUPPORT de sus implementaciones de **IMAPIProp::GetIDsFromNames** y **IMAPIProp::GetNamesFromIDs** . Para obtener más información, vea [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) y [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Debido a que las secciones del perfil no admiten transacciones, todos los cambios realizados con llamadas a **IMAPIProp::CopyProps**, **CopyTo**o **SetProps** surte efecto inmediatamente. Para obtener más información, vea [IMAPIProp::CopyProps](imapiprop-copyprops.md). Los clientes y proveedores de servicios pueden llamar (método **IMAPIProp::SaveChanges** ) de una sección de perfil y se realizará correctamente, pero no afecta a los datos de la sección de perfil. Para obtener más información, vea [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Necesidad de cambios se producen inmediatamente puede afectar a cómo los proveedores de servicios de implementan las hojas de propiedades que los clientes usan para mostrar las propiedades de perfil a los usuarios. Proveedores de servicios que desean que los usuarios puedan posponer o deshacer los cambios deben implementar sus hojas de propiedades con copias de las secciones de perfil en lugar de las secciones reales. Mediante el uso de copias, los usuarios pueden realizar cambios y, a continuación, más adelante cancelar los cambios, dejando intactos las secciones de perfil original. 
  
El orden en el que aparece la información en un perfil afecta a cómo MAPI configura los recursos y realiza las asignaciones en una sesión. Las siguientes asignaciones se ven afectadas por orden de perfiles:
  
- Almacén de mensajes predeterminado
    
- Libreta personal de direcciones
    
- Ruta de acceso de búsqueda de almacén de mensaje predeterminada
    
- Valor predeterminado de ruta de acceso de búsqueda de la libreta de direcciones
    
- Orden del proveedor de transporte
    
MAPI establece el almacén de mensajes predeterminado a ser el primer almacén de mensajes en el perfil que tiene la marca STATUS_DEFAULT_STORE establecer en su propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)), que indica que puede ser el almacén predeterminado. Los clientes pueden invalidar esta configuración mediante una llamada a **IMAPISession::SetDefaultStore**. Para obtener más información, vea [IMAPISession::SetDefaultStore](imapisession-setdefaultstore.md).
  
MAPI crea un pedido de transporte para el tratamiento de mensajes entrantes y salientes. Cuando más de un proveedor de transporte se ha registrado para un mensaje de un tipo determinado, MAPI usa este orden para determinar qué proveedor debe controlar el mensaje. MAPI establece el orden de transporte que será el orden en el que se colocan el transporte proveedores se han agregado al perfil con una excepción: los transportes de establecer la marca STATUS_XP_PREFER_LAST en su propiedad **PR_RESOURCE_FLAGS** por última vez en el orden. Los clientes pueden establecer el orden de transporte mediante una llamada a **IMsgServiceAdmin::MsgServiceTransportOrder**. Para obtener más información, vea [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
En ocasiones, es posible que entre en conflicto estas instrucciones para la ordenación de los proveedores de servicios y los servicios de mensajes. Si hay un conflicto, el código debe resolver el conflicto. Puede usar el programa de Panel de Control de correo para inspeccionar un perfil que haya creado para determinar si se han configurado los proveedores como se esperaba.
  

