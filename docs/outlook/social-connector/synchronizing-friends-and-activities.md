---
title: Sincronizar sus amigos y actividades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: Outlook Social Connector (OSC) admite mostrando información de una red social sobre una persona en la tarjeta de contacto o en el panel de personas de Outlook. SharePoint Server, SharePoint Workspace, cliente de Lync y todas las aplicaciones de cliente de Office que admiten la compatibilidad con la información de presencia la tarjeta de contacto.
ms.openlocfilehash: 9e843d8013b329a88de88232f16740edae77c1d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821219"
---
# <a name="synchronizing-friends-and-activities"></a>Sincronizar sus amigos y actividades

Outlook Social Connector (OSC) admite mostrando información de una red social sobre una persona en la tarjeta de contacto o en el panel de personas de Outlook. SharePoint Server, SharePoint Workspace, cliente de Lync y todas las aplicaciones de cliente de Office que admiten la compatibilidad con la información de presencia la tarjeta de contacto.
  
Puede usar la tarjeta de contacto en escenarios de colaboración en las aplicaciones de Office para obtener más información acerca de las personas a las que está colaborando con. Ejemplos de estos escenarios incluyen mensajería en Outlook y la co-autoría de un documento de Word. Al hacer clic en la ficha **Cuáles son las novedades** de una tarjeta de contacto, la muestra información acerca de esa persona. 
  
El panel de personas de Outlook muestra información acerca de una persona puede ser un remitente o destinatario de un elemento de Outlook que ha seleccionado. Cuando se selecciona a otra persona en el panel de personas u otro elemento en el Explorador de Outlook, o abra un elemento de Outlook en un inspector, Outlook Social Connector (OSC) actualiza el panel de personas. 
  
Para que la tarjeta de contacto o el panel de personas mostrar información actual de la persona seleccionada, el OSC sincroniza dicha información a través de los proveedores de OSC y algún tipo de almacenamiento en caché. Esta sincronización depende de los proveedores de OSC que están instalados en el equipo cliente, que inicien la sesión a través de sus proveedores de OSC y el modo de sincronización que cada uno de los proveedores de OSC para estas social redes compatible con las redes sociales.
  
El OSC admite sincronización amigos, que no sean de amigos y actividades de amigos y amigos que no sean de diferentes maneras: caché de sincronización, la sincronización a petición y la sincronización de híbrida. La diferencia principal entre estos modos de sincronización es donde el OSC almacena los datos, si está en una carpeta en el almacén de Outlook predeterminado del usuario o en la memoria en el equipo del usuario. En cada caso como se indicó en este tema, hay un valor predeterminado de tiempo mínimo que los datos permanezcan en la carpeta o la memoria antes de que se actualizan los datos. En algunos casos, la cantidad mínima de tiempo se puede personalizar mediante la directiva de grupo. Para obtener más información acerca de las directivas de grupo que controlan el comportamiento de la OSC, vea [cómo administrar Outlook Social Connector mediante la directiva de grupo](http://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103).
  
Tenga en cuenta que si la persona seleccionada no es un miembro de la red social, el OSC no se muestra ninguna información de la persona o la actividad de esa persona en la tarjeta de contacto o el panel de personas.
  
## <a name="cached-synchronization"></a>Sincronización de caché

Un proveedor de OSC puede almacenar información de amigos en la red social en una carpeta específica en el almacén de Outlook predeterminado del usuario y actualizar periódicamente esa memoria caché una vez transcurrido un período de tiempo especificado. Almacenamiento en caché de información en una carpeta tiene la ventaja de reducir el tráfico a la red social.
  
> [!NOTE]
> A partir de Outlook Social Connector 2013, el OSC ya no admite la sincronización de caché de actividades. 
  
### <a name="cached-synchronization-of-friends"></a>Sincronización de caché de amigos

Si un proveedor de OSC admite la sincronización en caché para amigos, el OSC recopila información de amigos del usuario que ha iniciado sesión en la red social. La información se almacena en caché en una carpeta de contactos de Outlook que es específica de esa red social en almacén de Outlook predeterminado del usuario. Nombre de la carpeta de contactos se basa en el nombre de la red social, que obtiene el OSC mediante el uso de la propiedad [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) . 
  
En la sincronización de caché, el OSC almacena información de solo los amigos del usuario que ha iniciado sesión en la red social. El OSC no tiene acceso a la información para que no sean de amigos.
  
El intervalo predeterminado para el OSC actualizar la carpeta de contactos para obtener información de amigos desde la red social es una vez al día (o una vez por cada 1.440 minutos). También se puede establecer este intervalo de actualización de directiva de grupo, como se ha explicado al principio de este tema.
  
Si se produce un error durante una actualización, el OSC reintenta en un intervalo especificado por el elemento **contactSyncRestartInterval** en el XML de las **capacidades** . Este intervalo de reintentos de tiene un valor predeterminado de 30 minutos y también se puede establecer mediante la directiva de grupo. 
  
Cuando un usuario abre una tarjeta de contacto y selecciona la ficha **Novedades** , actualiza la ficha **Cuáles son las novedades** . De forma similar, cuando un usuario de Outlook selecciona un elemento de Outlook o selecciona a una persona en el panel de personas, se actualiza el panel de personas. Si no ha expirado el intervalo de actualización de la memoria caché, el OSC se desvía a la memoria caché para obtener la información del usuario seleccionado. Esto evita la sobrecarga de uso de extensibilidad del proveedor OSC para tener acceso a la red social. Si ha caducado el intervalo de actualización, el OSC llama al método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obtener información sobre amigos actual para el usuario que ha iniciado la sesión y actualiza la memoria caché en la carpeta Contactos. 
  
El proveedor de OSC informa el OSC que admite la sincronización en caché de amigos mediante la especificación de los siguientes elementos en el XML de las **capacidades de** : 
  
- **getFriends** = **es true**
    
- **cacheFriends** = **es true**
    
- **dynamicContactsLookup** = **false**
    
## <a name="on-demand-synchronization"></a>Sincronización a petición

Cuando un usuario selecciona la ficha **Cuáles son las novedades** en una tarjeta de contacto, o selecciona un elemento de Outlook diferente o una persona diferente en el panel de personas en Outlook, el OSC actualiza la tarjeta de contacto o el panel de personas, respectivamente. Si un proveedor de OSC admite la sincronización a petición de las personas o actividades, el OSC se sincroniza con una memoria caché en la memoria y actualiza los detalles, como el nombre, título, imágenes y secuencias de actividad, en la tarjeta de contacto o el panel de personas. Para la sincronización a petición, a diferencia de sincronización de caché, el OSC intenta actualizar la información para la persona, independientemente de si esa persona es un amigo o que no sean amigo del usuario ha iniciado sesión en la red social. 
  
Datos de persona (o actividad) y a petición se almacenan sólo en la memoria. Los datos en memoria se borran cuando cierra la aplicación de cliente de Office, o el usuario produce una actualización de la tarjeta de contacto o el panel de personas y los datos ha permanecido en la memoria durante más tiempo que el intervalo de actualización. Tenga en cuenta que la actualización desde la red social siempre se inicia por un usuario actualizar la tarjeta de contacto o el panel de personas, (por ejemplo, mediante la selección de un usuario diferente en el panel de personas, o seleccione un elemento diferente en la ventana del explorador de Outlook). 

Sin embargo, lo contrario no es siempre true, no cada actualización de la tarjeta de contacto o el panel de personas necesariamente incurre en una actualización desde la red social. Si el usuario actualiza la tarjeta de contacto o datos del panel de personas y la persona (o actividad) ha permanecido en la memoria durante más tiempo que el intervalo de actualización, el OSC llamadas [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) (o [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)) a actualizar la información en la memoria desde la red social. El período de permitidos para obtener información de amigo y que no sean de confianza en la memoria es de 24 horas y para las actividades, 30 minutos. 
  
Una diferencia importante entre la sincronización de almacenado en caché y a petición es que la sincronización a petición puede obtener información de la persona y la actividad de amigos y amigos que no sean en la red. Si la persona seleccionada es un amigo-que no sean, el OSC actualiza la información y las actividades de esa persona si se cumple cualquiera de los siguientes requisitos: 
  
- La persona es un usuario de la red social y permite la visualización pública de la información de perfil y actividad.
    
- La persona está en la misma red que el usuario ha iniciado la sesión de esa red social (por ejemplo, en la misma red para alumnos Universidad).
    
Sincronización a petición de los resultados de las personas y las actividades en más llamadas para el proveedor desde el motor de núcleo OSC. Redes sociales deben ser capaces de controlar los requisitos de ancho de banda aumentado de sincronización a petición.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Especificación de los elementos XML para la sincronización a petición

El proveedor de OSC informa el OSC que admite sincronización a petición de amigos y que no sean de amigos mediante la especificación de los siguientes elementos en el XML de las **capacidades de** : 
  
- **getFriends** = **es true**
    
- **cacheFriends** = **false**
    
- **dynamicContactsLookup** = **es true**
    
El proveedor de OSC informa el OSC que admite la sincronización a petición de actividades mediante la especificación de los siguientes elementos en el XML de las **capacidades de** : 
  
- **getActivities** = **es true**
    
- **cacheActivities** = **false**
    
- **dynamicActivitiesLookupEx** = **es true**
    
## <a name="hybrid-synchronization"></a>Sincronización de híbrido

Un proveedor de OSC puede admitir sincronización híbrido de amigos y amigos que no sean. Esto puede optimizar las llamadas entre el motor de núcleo OSC y el proveedor de OSC, las llamadas a la red social para la sincronización a petición de amigos y la moneda de los datos de los amigos. El tiempo mínimo que pueden permanecer los datos en una carpeta o la memoria, en su caso, es igual a los límites indicados en los modos de sincronización a petición o almacenados en caché.
  
> [!NOTE]
> A partir de Outlook Social Connector 2013, el OSC admite sólo la sincronización a petición de actividades y ya no admite la sincronización de híbrido de actividades. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Sincronización de híbrido de amigos y amigos que no sean

Si un proveedor de OSC admite la sincronización de híbrido de amigos y amigos que no sean, el OSC hace lo siguiente: 
  
- El OSC almacena información de amigos del usuario que ha iniciado sesión en la carpeta de contactos específica de la red social.
    
- El OSC almacena información para que no sean de amigos del usuario que ha iniciado sesión en la memoria.
    
El proveedor de OSC informa el OSC que admite sincronización híbrido de amigos y que no sean de amigos mediante la especificación de los siguientes elementos en el XML de las **capacidades de** : 
  
- **getFriends** = **es true**
    
- **cacheFriends** = **es true**
    
- **dynamicContactsLookup** = **es true**
    
## <a name="synchronization-intervals"></a>Intervalos de sincronización

En la siguiente tabla se resume los intervalos de la sincronización de amigos y amigos que no sean de información entre la memoria caché correspondiente (carpeta o memoria) y las redes sociales, según el modo de sincronización compatible. Para el modo de sincronización de híbrido, hacer referencia a las filas para el modo caché de amigos y la fila para el modo para que no sean de amigos y a petición.
  
|**Modo de sincronización de personas**|**Donde se establece el intervalo de actualización**|**Valor predeterminado de tiempo mínimo antes de la actualización**|**Invalidar la directiva de grupo**|
|:-----|:-----|:-----|:-----|
|Cached  <br/> |Establecer dentro de OSC  <br/> |1440 minutos (24 horas)  <br/> |Valor del registro de Windows **NetContactSyncInterval** <br/> |
|Cached  <br/> |elemento **contactSyncRestartInterval** en las **capacidades** de XML  <br/> |30 minutos si no se ha establecido **contactSyncRestartInterval**  <br/> |De valor del registro de Windows **contactSyncRestartInterval** <br/> |
|Bajo demanda  <br/> |Establecer dentro de OSC  <br/> |1440 minutos (24 horas)  <br/> |Valor del registro de Windows **OnlineSearchExpiryTime** <br/> |
   
En la siguiente tabla se resume los intervalos de sincronización de actividades de amigos y amigos entre la caché correspondiente (carpeta o memoria) y la red social, dependiendo de los modos de sincronización compatible. 
  
|**Modo de sincronización de actividades**|**Donde se establece el intervalo de actualización**|**Valor predeterminado de tiempo mínimo antes de la actualización**|**Invalidar la directiva de grupo**|
|:-----|:-----|:-----|:-----|
|Bajo demanda  <br/> |Establecer dentro de OSC  <br/> |30 minutos  <br/> |Valor del registro de Windows **OnlineSearchExpiryTime** <br/> |
   
La siguiente información se aplica a los valores del registro de Windows que aparecen en las dos tablas:
  
- Clave:`HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- Valor: Valor DWORD entre 1 y 10080
    
## <a name="see-also"></a>Vea también

- [Ejemplo de XML de capacidades](capabilities-xml-example.md)  
- [XML de capacidades](xml-for-capabilities.md)
- [Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Cómo administrar Outlook Social Connector mediante la directiva de grupo](http://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

