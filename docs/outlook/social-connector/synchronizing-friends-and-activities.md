---
title: Sincronizar sus amigos y actividades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: Outlook Social Connector (OSC) admite la visualización de información de una red social sobre una persona en la tarjeta de contacto o en el panel de personas de Outlook. SharePoint Server, SharePoint Workspace, cliente de Lync y todas las aplicaciones cliente de Office que admiten la información de presencia admiten la tarjeta de contacto.
ms.openlocfilehash: 0d6881c5d596519422d01ca61a00b1a68e610f2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329204"
---
# <a name="synchronizing-friends-and-activities"></a>Sincronizar sus amigos y actividades

Outlook Social Connector (OSC) admite la visualización de información de una red social sobre una persona en la tarjeta de contacto o en el panel de personas de Outlook. SharePoint Server, SharePoint Workspace, cliente de Lync y todas las aplicaciones cliente de Office que admiten la información de presencia admiten la tarjeta de contacto.
  
Puede usar la tarjeta de contacto en escenarios de colaboración en las aplicaciones de Office para obtener más información sobre las personas con las que está colaborando. Algunos ejemplos de estos escenarios incluyen la mensajería en Outlook y la co-autoría en un documento de Word. Al hacer clic en **** la pestaña novedades de una tarjeta de contacto, el muestra información sobre esa persona. 
  
El panel de personas de Outlook muestra información sobre una persona que puede ser un remitente o un destinatario de un elemento de Outlook que haya seleccionado. Siempre que seleccione a otra persona en el panel de personas o a otro elemento en el explorador de Outlook, o abra un elemento de Outlook en un inspector, Outlook Social Connector (OSC) actualizará el panel de personas. 
  
En el caso de la tarjeta de contacto o el panel de personas para mostrar la información actual de la persona seleccionada, el OSC sincroniza la información a través de los proveedores de OSC y alguna forma de almacenamiento en caché. Esta sincronización depende de los proveedores de OSC instalados en el equipo cliente, las redes sociales en las que ha iniciado sesión a través de sus proveedores de OSC y el modo de sincronización que admite cada uno de los proveedores de OSC para estas redes sociales.
  
El OSC permite sincronizar amigos, no amigos y actividades de amigos y no amigos de distintas formas: sincronización en caché, sincronización a petición y sincronización híbrida. La diferencia principal entre estos modos de sincronización es cuando el OSC almacena los datos, ya sea en una carpeta en el almacén de Outlook predeterminado del usuario o en la memoria del equipo del usuario. En cada caso, tal y como se indica en este tema, hay un tiempo mínimo predeterminado para que los datos permanezcan en la carpeta o en la memoria antes de que se actualicen los datos. En algunos casos, la Directiva de grupo puede personalizar la cantidad mínima de tiempo. Para obtener más información acerca de las directivas de grupo que controlan el comportamiento de OSC, consulte [How to Manage the Outlook Social Connector by Using Group Policy](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103).
  
Tenga en cuenta que si la persona seleccionada no es miembro de la red social, OSC no muestra ninguna persona o información de actividad de esa persona en el panel de la tarjeta de contacto o de personas.
  
## <a name="cached-synchronization"></a>Sincronización en caché

Un proveedor OSC puede almacenar información para amigos en la red social en una carpeta específica del almacén de Outlook predeterminado del usuario y actualizar periódicamente dicha caché una vez transcurrido un período de tiempo especificado. El almacenamiento en caché de la información en una carpeta tiene la ventaja de reducir el tráfico a la red social.
  
> [!NOTE]
> A partir de Outlook Social Connector 2013, el OSC ya no admite la sincronización de actividades almacenada en caché. 
  
### <a name="cached-synchronization-of-friends"></a>Sincronización de amigos en caché

Si un proveedor de OSC admite la sincronización en caché para amigos, el OSC almacena en caché la información de los amigos del usuario que ha iniciado sesión en la red social. La información se almacena en caché en una carpeta de contactos de Outlook que es específica de esa red social en la tienda de Outlook predeterminada del usuario. El nombre de la carpeta de contactos se basa en el nombre de la red social, que el OSC obtiene mediante la propiedad [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) . 
  
En la sincronización en caché, el OSC almacena información sólo de los amigos del usuario que ha iniciado sesión en la red social. El OSC no tiene acceso a la información de personas que no sean amigos.
  
El intervalo predeterminado para que el OSC actualice la carpeta de contactos para la información de los amigos desde la red social es una vez por día (o una vez por 1440 minutos). Este intervalo de actualización también puede establecerse mediante la Directiva de grupo, como se ha explicado al principio de este tema.
  
Si se produce un error durante una actualización, el OSC reintenta en un intervalo especificado por el elemento **contactSyncRestartInterval** en el XML de **funciones** . Este intervalo de reintento tiene un valor predeterminado de 30 minutos y también puede establecerse mediante la Directiva de grupo. 
  
Cuando un usuario abre una tarjeta de contacto y selecciona **** la pestaña novedades, se actualiza **** la pestaña novedades. De forma similar, cuando un usuario de Outlook reselecciona un elemento en Outlook o reselecciona una persona en el panel de personas, el panel de personas se actualiza. Si el intervalo de actualización de caché no ha expirado, el OSC se dirige a la memoria caché para obtener la información del usuario seleccionado. Esto evita la sobrecarga de usar la extensibilidad de proveedores de OSC para obtener acceso a la red social. Si el intervalo de actualización ha expirado, el OSC llama al método [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obtener la información actual de los amigos para el usuario que ha iniciado sesión y actualiza la memoria caché de la carpeta contactos. 
  
El proveedor OSC informa a OSC de que admite la sincronización de amigos en caché especificando los siguientes elementos en el XML de **capacidades** : 
  
- **getFriends** = **true**
    
- **cacheFriends** = **true**
    
- **dynamicContactsLookup** = **false**
    
## <a name="on-demand-synchronization"></a>Sincronización a petición

Cuando un usuario selecciona la **** pestaña novedades en una tarjeta de contacto, o selecciona un elemento de Outlook diferente o una persona distinta en el panel de personas en Outlook, OSC actualiza la tarjeta de contacto o el panel de personas, respectivamente. Si un proveedor de OSC admite la sincronización a petición de personas o actividades, el OSC se sincroniza con una memoria caché en la memoria y actualiza los detalles, como el nombre, el título, la imagen y las secuencias de actividades, en el panel de la tarjeta de contacto o de las personas. Para la sincronización a petición, a diferencia de la sincronización en caché, el OSC intenta actualizar la información de la persona independientemente de si esa persona es un amigo o no es amigo del usuario que ha iniciado sesión en la red social. 
  
Los datos de la persona (o actividad) a petición se almacenan solo en la memoria. Los datos en memoria se borran cuando se cierra la aplicación cliente de Office o el usuario causa una actualización de la tarjeta de contacto o el panel de personas y los datos se han mantenido en la memoria durante más tiempo que el intervalo de actualización. Tenga en cuenta que la actualización de la red social siempre es iniciada por un usuario que actualice la tarjeta de contacto o el panel de personas (por ejemplo, seleccionando un usuario diferente en el panel de personas o seleccionando un elemento diferente en la ventana del explorador de Outlook). 

Sin embargo, el valor inverso no siempre es verdadero; no todas las actualizaciones de la tarjeta de contacto o el panel de personas incurren necesariamente en una actualización desde la red social. Si el usuario actualiza la tarjeta de contacto o el panel de personas y los datos de la persona (o actividad) han permanecido en la memoria durante más tiempo que el intervalo de actualización, el OSC llama a [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md) (o [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)) para actualizar la información de la memoria de la red social. El período permitido para la información de amigos y no amigos en la memoria es de 24 horas y para las actividades de 30 minutos. 
  
Una diferencia importante entre la sincronización a petición y la caché es que la sincronización a petición puede recuperar la información de la persona y la actividad de los amigos y de los que no son amigos de la red. Si la persona seleccionada no es Friend, el OSC actualiza la información y las actividades de esa persona si se cumple alguno de los siguientes requisitos: 
  
- La persona es un usuario de la red social y permite ver la información de la actividad y del perfil.
    
- La persona está en la misma red que el usuario que ha iniciado sesión en esa red social (por ejemplo, en la misma red para los ex alumnos de la Universidad).
    
La sincronización a petición de personas y actividades da como resultado más llamadas al proveedor desde el motor del núcleo OSC. Las redes sociales deben poder administrar los requisitos de ancho de banda aumentados de la sincronización a petición.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Especificación de elementos XML para la sincronización a petición

El proveedor OSC informa a OSC de que admite la sincronización a petición de amigos y no amigos especificando los siguientes elementos en el XML de **capacidades** : 
  
- **getFriends** = **true**
    
- **cacheFriends** = **false**
    
- **dynamicContactsLookup** = **true**
    
El proveedor OSC informa a OSC de que admite la sincronización a petición de las actividades mediante la especificación de los siguientes elementos en el XML de **capacidades** : 
  
- **getActivities** = **true**
    
- **cacheActivities** = **false**
    
- **dynamicActivitiesLookupEx** = **true**
    
## <a name="hybrid-synchronization"></a>Sincronización híbrida

Un proveedor OSC puede admitir la sincronización híbrida de amigos y no amigos. Esto puede optimizar las llamadas entre el motor del núcleo OSC y el proveedor de OSC, las llamadas a la red social para la sincronización a petición de amigos y la moneda de los datos de los amigos. El tiempo mínimo que pueden permanecer los datos en una carpeta o en la memoria, si corresponde, es el mismo que los límites de los modos de sincronización en caché o a petición.
  
> [!NOTE]
> A partir de Outlook Social Connector 2013, el OSC solo admite la sincronización a petición de actividades y ya no admite la sincronización híbrida de actividades. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Sincronización híbrida de amigos y no amigos

Si un proveedor de OSC admite la sincronización híbrida de amigos y no amigos, el OSC hace lo siguiente: 
  
- El OSC almacena información para amigos del usuario que ha iniciado sesión en la carpeta de contactos de redes sociales específicas.
    
- El OSC almacena información para no amigos del usuario que ha iniciado sesión en la memoria.
    
El proveedor OSC informa a OSC de que admite la sincronización híbrida de amigos y no amigos especificando los siguientes elementos en el XML de **capacidades** : 
  
- **getFriends** = **true**
    
- **cacheFriends** = **true**
    
- **dynamicContactsLookup** = **true**
    
## <a name="synchronization-intervals"></a>Intervalos de sincronización

En la tabla siguiente se resumen los intervalos de sincronización para información sobre amigos y no amigos entre la memoria caché correspondiente (carpeta o memoria) y la red social, según el modo de sincronización admitido. Para el modo de sincronización híbrida, consulte las filas del modo en caché para los amigos y la fila de modo a petición para los que no sean amigos.
  
|**Modo de sincronización para personas**|**Donde se establece el intervalo de actualización**|**Tiempo mínimo predeterminado antes de la actualización**|**Invalidación de la Directiva de grupo**|
|:-----|:-----|:-----|:-----|
|Cached  <br/> |Establecido en OSC  <br/> |1440 minutos (24 horas)  <br/> |Valor del registro de Windows **NetContactSyncInterval** <br/> |
|Cached  <br/> |elemento **contactSyncRestartInterval** en el código XML de **capacidades**  <br/> |30 minutos si no se establece **contactSyncRestartInterval**  <br/> |Valor del registro de Windows **contactSyncRestartInterval** <br/> |
|Bajo demanda  <br/> |Establecido en OSC  <br/> |1440 minutos (24 horas)  <br/> |Valor del registro de Windows **OnlineSearchExpiryTime** <br/> |
   
En la tabla siguiente se resumen los intervalos de sincronización para actividades de amigos y no amigos entre la memoria caché correspondiente (carpeta o memoria) y la red social, en función de los modos de sincronización admitidos. 
  
|**Modo de sincronización para actividades**|**Donde se establece el intervalo de actualización**|**Tiempo mínimo predeterminado antes de la actualización**|**Invalidación de la Directiva de grupo**|
|:-----|:-----|:-----|:-----|
|Bajo demanda  <br/> |Establecido en OSC  <br/> |30 minutos  <br/> |Valor del registro de Windows **OnlineSearchExpiryTime** <br/> |
   
La siguiente información se aplica a los valores del registro de Windows que aparecen en las dos tablas:
  
- Fundamental`HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- Valor: valor DWORD entre 1 y 10080
    
## <a name="see-also"></a>Vea también

- [Ejemplo de XML de capacidades](capabilities-xml-example.md)  
- [XML para funcionalidades](xml-for-capabilities.md)
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Procedimiento para administrar Outlook Social Connector mediante la Directiva de grupo](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

