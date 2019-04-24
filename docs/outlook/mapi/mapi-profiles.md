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
  
Un perfil almacena información sobre los proveedores de servicios y los servicios de mensajes que están instalados en un equipo. Para cada sesión, un cliente en el momento del inicio de sesión selecciona un perfil que describe los proveedores y los servicios que se van a usar. Un cliente puede elegir entre una colección de perfiles y, si lo desea, establecer uno como predeterminado. El perfil predeterminado es el perfil que se selecciona automáticamente cuando un cliente inicia una sesión y no ha especificado explícitamente un perfil.
  
En estos temas también encontrará una descripción de la caché de sobrenombres, que se almacena en una secuencia binaria.
  
- [Caché de alias](nickname-cache.md)
    
- [Secuencia de autocompletar](autocomplete-stream.md)
    
- [Análisis de archivos binarios](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Secciones de perfil

Los perfiles se dividen en secciones a las que tienen acceso los clientes y los proveedores de servicios para mostrar las propiedades de perfil a los usuarios o para realizar cambios en la configuración. Una sección de perfil es un objeto MAPI que implementa la interfaz **IProfSect** , una interfaz que deriva de **IMAPIProp** y no tiene métodos adicionales. Para obtener más información, vea [IProfSect: IMAPIProp](iprofsectimapiprop.md). Su único propósito es manipular las propiedades de una sección de perfil. Para recuperar un puntero **IProfSect** a una sección de perfil determinada, los clientes y los proveedores de servicios llaman a los métodos siguientes. 
  
|||
|:-----|:-----|
|Los clientes pueden llamar a:  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Los proveedores de servicios pueden llamar a:  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Los clientes o proveedores pueden llamar a:  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Los perfiles se organizan jerárquicamente de manera similar a los MAPISVC. Archivo INF. En la parte superior de la jerarquía, hay secciones de perfil que contienen información relevante para el perfil. El nivel intermedio incluye secciones que contienen información acerca de un servicio de mensajes en particular y el nivel inferior incluye secciones que contienen información sobre uno de los proveedores de servicios de un servicio de mensajes. 
  
Cada perfil tiene varias propiedades requeridas que se almacenan en una o varias de las secciones del perfil. Por ejemplo, cada perfil tiene las propiedades **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). La clave de búsqueda de un perfil se establece en el valor definido en MAPIGUID. H como MUID_PROFILE_INSTANCE y siempre se garantiza que sea único entre todos los perfiles. Aunque dos perfiles pueden tener el mismo nombre, no pueden tener la misma clave de búsqueda. Las claves de búsqueda deben tratarse como datos binarios en lugar de datos de cualquier tipo en particular.
  
Los proveedores de almacenamiento de mensajes son necesarios para incluir la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) del almacén de mensajes en las secciones de perfil para el perfil y para su proveedor de almacenamiento de mensajes y mantener estas entradas sincronizadas. Cuando se crea un almacén de mensajes, el proveedor establece **PR_DISPLAY_NAME** basándose en el valor almacenado en estas secciones de perfil. 
  
Hay dos diferencias principales entre las secciones de perfil y otros objetos que heredan de **IMAPIProp**: 
  
- Las secciones de perfil no admiten transacciones.
    
- Las secciones de perfil no admiten propiedades con nombre y devuelven MAPI_E_NO_SUPPORT de sus implementaciones **IMAPIProp:: GetIDsFromNames** y **IMAPIProp:: GetNamesFromIDs** . Para obtener más información, vea [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) y [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Como las secciones de perfil no admiten transacciones, los cambios realizados con llamadas a **IMAPIProp:: CopyProps**, **CopyTo**o **SetProps** se aplican inmediatamente. Para obtener más información, vea [IMAPIProp:: CopyProps](imapiprop-copyprops.md). Los clientes y los proveedores de servicios pueden llamar al método **IMAPIProp:: SaveChanges** de una sección de perfil y funcionarán correctamente, pero no afectan a los datos de la sección del perfil. Para obtener más información, vea [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). El hecho de que los cambios se produzcan inmediatamente puede afectar a cómo los proveedores de servicios implementan las hojas de propiedades que los clientes usan para mostrar las propiedades de perfil a los usuarios. Los proveedores de servicios que desean que los usuarios puedan posponer o deshacer los cambios deben implementar sus hojas de propiedades con copias de secciones de perfil en lugar de las secciones reales. Mediante el uso de copias, los usuarios pueden realizar cambios y, posteriormente, cancelar los cambios, dejando las secciones de perfil originales inalteradas. 
  
El orden en el que la información aparece en un perfil afecta a la forma en que MAPI configura los recursos y realiza asignaciones en una sesión. Las siguientes asignaciones se ven afectadas por el orden de los perfiles:
  
- Almacén de mensajes predeterminado
    
- Libreta personal de direcciones
    
- Ruta de búsqueda predeterminada del almacén de mensajes
    
- Ruta de búsqueda predeterminada de la libreta de direcciones
    
- Orden de proveedores de transporte
    
MAPI establece el almacén de mensajes predeterminado como el primer almacén de mensajes en el perfil que tiene la marca STATUS_DEFAULT_STORE establecida en su propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)), lo que indica que puede ser el almacén predeterminado. Los clientes pueden invalidar esta configuración llamando a **IMAPISession:: SetDefaultStore**. Para obtener más información, vea [IMAPISession:: SetDefaultStore](imapisession-setdefaultstore.md).
  
MAPI crea un orden de transporte para controlar los mensajes entrantes y salientes. Cuando se registra más de un proveedor de transporte para un mensaje de un tipo determinado, MAPI usa este orden para determinar qué proveedor debe controlar el mensaje. MAPI establece que el orden de transporte sea el orden en que se agregaron los proveedores de transporte al perfil con una excepción: los transportes que establecen la marca STATUS_XP_PREFER_LAST en su propiedad **PR_RESOURCE_FLAGS** se colocan en el último lugar en el orden. Los clientes pueden establecer el orden de transporte llamando a **IMsgServiceAdmin:: MsgServiceTransportOrder**. Para obtener más información, vea [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Estas instrucciones para solicitar los proveedores de servicios y los servicios de mensajes podrían a veces entrar en conflicto. Si hay un conflicto, el código debe resolver el conflicto. Puede usar el programa del panel de control de correo para inspeccionar un perfil que haya creado para determinar si los proveedores se han configurado como se esperaba.
  

