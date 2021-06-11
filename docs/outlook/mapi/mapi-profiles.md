---
title: Perfiles MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 493c87a4-317d-47ec-850b-342cac59594b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9db1f8e163e44a44df1e798cebccb3639325275e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340085"
---
# <a name="mapi-profiles"></a>Perfiles MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un perfil almacena información sobre los proveedores de servicios y los servicios de mensajes que están instalados en un equipo. Para cada sesión, un cliente en el momento del inicio de sesión selecciona un perfil que describe los proveedores y servicios que se usarán. Un cliente puede elegir entre una colección de perfiles y, si lo desea, establecer uno como predeterminado. El perfil predeterminado es el perfil que se selecciona automáticamente cuando un cliente inicia una sesión y no ha especificado explícitamente un perfil.
  
También en estos temas, encontrará una discusión sobre la caché de alias, que se almacena en una secuencia binaria.
  
- [Caché de alias](nickname-cache.md)
    
- [Secuencia de autocompletar](autocomplete-stream.md)
    
- [Análisis de archivos binarios](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Secciones de perfil

Los perfiles se dividen en secciones a las que los clientes y proveedores de servicios tienen acceso para mostrar propiedades de perfil a los usuarios o para realizar cambios en la configuración. Una sección de perfil es un objeto MAPI que implementa la interfaz **IProfSect,** una interfaz que deriva de **IMAPIProp** y no tiene métodos adicionales. Para obtener más información, vea [IProfSect : IMAPIProp](iprofsectimapiprop.md). Su único propósito es manipular las propiedades de una sección de perfil. Para recuperar un **puntero IProfSect** a una sección de perfil determinada, los clientes y proveedores de servicios llaman a los métodos siguientes. 
  
|||
|:-----|:-----|
|Los clientes pueden llamar a:  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Los proveedores de servicios pueden llamar a:  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Los clientes o proveedores pueden llamar a:  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Los perfiles se organizan jerárquicamente de forma muy parecido a MAPISVC. Archivo INF. En la parte superior de la jerarquía, hay secciones de perfil que contienen información relevante para el perfil. El nivel medio incluye secciones que contienen información sobre un servicio de mensajes en particular y el nivel inferior incluye secciones que contienen información sobre uno de los proveedores de servicios de un servicio de mensajes. 
  
Cada perfil tiene varias propiedades necesarias que se almacenan en una o más de las secciones del perfil. Por ejemplo, cada perfil tiene las propiedades **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). La clave de búsqueda de un perfil se establece en el valor definido en MAPIGUID. H como MUID_PROFILE_INSTANCE y siempre se garantiza que sea único entre todos los perfiles. Aunque dos perfiles pueden tener el mismo nombre, no pueden tener la misma clave de búsqueda. Las claves de búsqueda deben tratarse como datos binarios en lugar de datos de cualquier tipo en particular.
  
Los proveedores de almacén de mensajes deben incluir la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de su almacén de mensajes en las secciones de perfil para el perfil y para su proveedor de almacén de mensajes y para mantener estas entradas sincronizadas. Cuando se crea un almacén de mensajes, el proveedor **establece PR_DISPLAY_NAME** en función del valor almacenado en estas secciones de perfil. 
  
Hay dos diferencias principales entre las secciones de perfil y otros objetos que heredan de **IMAPIProp:** 
  
- Las secciones de perfil no admiten transacciones.
    
- Las secciones de perfil no admiten propiedades con nombre y devuelven MAPI_E_NO_SUPPORT de sus implementaciones **IMAPIProp::GetIDsFromNames** e **IMAPIProp::GetNamesFromIDs.** Para obtener más información, vea [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Dado que las secciones de perfil no admiten transacciones, los cambios realizados con llamadas a **IMAPIProp::CopyProps**, **CopyTo** o **SetProps** tienen efecto inmediatamente. Para obtener más información, [vea IMAPIProp::CopyProps](imapiprop-copyprops.md). Los clientes y proveedores de servicios pueden llamar al método **IMAPIProp::SaveChanges** de una sección de perfil y se realizará correctamente, pero no afecta a los datos de la sección de perfil. Para obtener más información, [vea IMAPIProp::SaveChanges](imapiprop-savechanges.md). Si se producen cambios inmediatamente, los proveedores de servicios implementan las hojas de propiedades que los clientes usan para mostrar propiedades de perfil a los usuarios. Los proveedores de servicios que desean que los usuarios puedan posponer o deshacer los cambios deben implementar sus hojas de propiedades con copias de secciones de perfil en lugar de las secciones reales. Mediante el uso de copias, los usuarios pueden realizar cambios y, posteriormente, cancelarlos, dejando las secciones de perfil originales sin tocar. 
  
El orden en que aparece la información en un perfil afecta a la forma en que MAPI configura los recursos y realiza asignaciones en una sesión. El orden de perfil afecta a las siguientes asignaciones:
  
- Almacén de mensajes predeterminado
    
- Libreta de direcciones personal
    
- Ruta de búsqueda predeterminada del almacén de mensajes
    
- Ruta de búsqueda predeterminada de libreta de direcciones
    
- Pedido del proveedor de transporte
    
MAPI establece el almacén de mensajes predeterminado como el primer almacén de mensajes del perfil que tiene la marca de STATUS_DEFAULT_STORE establecida en su propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)), lo que indica que puede ser el almacén predeterminado. Los clientes pueden invalidar esta configuración llamando a **IMAPISession::SetDefaultStore**. Para obtener más información, [vea IMAPISession::SetDefaultStore](imapisession-setdefaultstore.md).
  
MAPI crea un orden de transporte para controlar los mensajes salientes y entrantes. Cuando más de un proveedor de transporte se ha registrado para un mensaje de un tipo determinado, MAPI usa este orden para determinar qué proveedor debe controlar el mensaje. MAPI establece el orden de transporte para que sea el orden en el que los proveedores de transporte se agregaron al perfil con una excepción: los transportes que establecen la marca STATUS_XP_PREFER_LAST en su propiedad **PR_RESOURCE_FLAGS** se sitúan en último lugar en el orden. Los clientes pueden establecer el orden de transporte llamando a **IMsgServiceAdmin::MsgServiceTransportOrder**. Para obtener más información, vea [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Estas directrices para ordenar los proveedores de servicios y los servicios de mensajes a veces pueden estar en conflicto. Si hay un conflicto, el código debe resolver el conflicto. Puede usar el programa Panel de control de correo para inspeccionar un perfil que haya creado para determinar si los proveedores se han configurado según lo esperado.
  

