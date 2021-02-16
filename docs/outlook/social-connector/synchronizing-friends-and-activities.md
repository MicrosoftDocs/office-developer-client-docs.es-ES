---
title: Sincronizar sus amigos y actividades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: Outlook Social Connector (OSC) admite mostrar información de una red social acerca de una persona en la tarjeta de contacto o en el panel de personas de Outlook. SharePoint Server, SharePoint Workspace, cliente lync y todas las aplicaciones cliente de Office que admiten información de presencia admiten la tarjeta de contacto.
ms.openlocfilehash: 0d6881c5d596519422d01ca61a00b1a68e610f2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329204"
---
# <a name="synchronizing-friends-and-activities"></a>Sincronizar sus amigos y actividades

Outlook Social Connector (OSC) admite mostrar información de una red social acerca de una persona en la tarjeta de contacto o en el panel de personas de Outlook. SharePoint Server, SharePoint Workspace, cliente lync y todas las aplicaciones cliente de Office que admiten información de presencia admiten la tarjeta de contacto.
  
Puede usar la tarjeta de contacto en escenarios de colaboración en aplicaciones de Office para obtener más información sobre las personas con las que está colaborando. Algunos ejemplos de estos escenarios son la mensajería en Outlook y la co-autoría de un documento en Word. Al hacer clic en **la pestaña Novedades de** una tarjeta de contacto, se muestra información sobre esa persona. 
  
El panel de personas de Outlook muestra información sobre una persona que puede ser un remitente o destinatario de un elemento de Outlook que ha seleccionado. Siempre que seleccione otra persona en el panel de personas u otro elemento en el explorador de Outlook, o abra un elemento de Outlook en un inspector, Outlook Social Connector (OSC) actualiza el panel de personas. 
  
Para que la tarjeta de contacto o el panel de personas muestre la información actual de la persona seleccionada, el OSC sincroniza dicha información a través de los proveedores de OSC y algún tipo de almacenamiento en caché. Esta sincronización depende de los proveedores de OSC instalados en el equipo cliente, las redes sociales en las que ha iniciado sesión a través de sus proveedores de OSC y el modo de sincronización que admite cada uno de los proveedores de OSC para estas redes sociales.
  
El OSC admite la sincronización de amigos, no amigos y actividades para amigos y no amigos de diferentes formas: sincronización en caché, sincronización a petición y sincronización híbrida. La principal diferencia entre estos modos de sincronización es cuando el OSC almacena los datos, ya sea en una carpeta del almacén predeterminado de Outlook del usuario o en la memoria del equipo del usuario. En cada caso, como se indica en este tema, hay un tiempo mínimo predeterminado que los datos permanecen en la carpeta o memoria antes de que se actualicen los datos. En algunos casos, la cantidad mínima de tiempo se puede personalizar mediante la directiva de grupo. Para obtener más información acerca de las directivas de grupo que controlan el comportamiento del OSC, vea Cómo administrar [Outlook Social Connector mediante la directiva de grupo.](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)
  
Tenga en cuenta que si la persona seleccionada no es miembro de la red social, el OSC no muestra ninguna persona o información de actividad para esa persona en la tarjeta de contacto o en el panel de personas.
  
## <a name="cached-synchronization"></a>Sincronización en caché

Un proveedor de OSC puede almacenar información para amigos en la red social en una carpeta específica del almacén predeterminado de Outlook del usuario y actualizar periódicamente esa memoria caché después de un período de tiempo especificado. El almacenamiento en caché de la información de una carpeta tiene la ventaja de reducir el tráfico a la red social.
  
> [!NOTE]
> A partir de Outlook Social Connector 2013, el OSC ya no admite la sincronización de actividades en caché. 
  
### <a name="cached-synchronization-of-friends"></a>Sincronización en caché de amigos

Si un proveedor de OSC admite la sincronización en caché para los amigos, el OSC almacena en caché la información de los amigos del usuario que ha iniciado sesión en la red social. La información se almacena en caché en una carpeta de contactos de Outlook que es específica de esa red social en el almacén de Outlook predeterminado del usuario. El nombre de la carpeta de contactos se basa en el nombre de la red social, que el OSC obtiene mediante la propiedad [ISocialProvider::SocialNetworkName.](isocialprovider-socialnetworkname.md) 
  
En la sincronización almacenada en caché, el OSC almacena información solo para los amigos del usuario que ha iniciado sesión en la red social. El OSC no tiene acceso a la información de los usuarios que no son amigos.
  
El intervalo predeterminado para que el OSC actualice la carpeta de contactos para obtener información de amigos de la red social es una vez al día (o una vez cada 1440 minutos). Este intervalo de actualización también se puede establecer mediante una directiva de grupo, como se describe al principio de este tema.
  
Si se produce un error durante una actualización, el OSC vuelve a insondizar en un intervalo especificado por el elemento **contactSyncRestartInterval** en el XML **de funcionalidades.** Este intervalo de reintentos tiene un valor predeterminado de 30 minutos y también se puede establecer mediante una directiva de grupo. 
  
Cuando un usuario abre una tarjeta  de contacto y selecciona la pestaña Novedades, se actualiza **la** pestaña Novedades. Del mismo modo, cuando un usuario de Outlook vuelve a seleccionar un elemento en Outlook o vuelve a seleccionar a una persona en el panel de personas, se actualiza el panel de personas. Si el intervalo de actualización de caché no ha expirado, el OSC se va a la memoria caché para obtener información del usuario seleccionado. Esto evita la sobrecarga de usar la extensibilidad del proveedor de OSC para acceder a la red social. Si el intervalo de actualización ha expirado, el OSC llama al método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obtener la información actual de los amigos del usuario que ha iniciado sesión y actualiza la memoria caché en la carpeta de contactos. 
  
El proveedor de OSC informa al OSC de que admite la sincronización en caché de amigos especificando los siguientes elementos en el XML **de funcionalidades:** 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **true**
    
- **dynamicContactsLookup**  =  **false**
    
## <a name="on-demand-synchronization"></a>Sincronización a petición

Cuando un usuario  selecciona la pestaña Novedades de una tarjeta de contacto o selecciona un elemento de Outlook diferente o una persona diferente en el panel de personas de Outlook, el OSC actualiza la tarjeta de contacto o el panel de personas respectivamente. Si un proveedor de OSC admite la sincronización a petición de personas o actividades, el OSC se sincroniza con una memoria caché y actualiza los detalles, como el nombre, el título, la imagen y las secuencias de actividades, en la tarjeta de contacto o en el panel de personas. Para la sincronización a petición, a diferencia de la sincronización almacenada en caché, el OSC intenta actualizar la información de la persona independientemente de si esa persona es un amigo o no amigo del usuario que ha iniciado sesión en la red social. 
  
Los datos de persona a petición (o actividad) solo se almacenan en la memoria. Los datos en memoria se borran cuando se cierra la aplicación cliente de Office o el usuario hace una actualización de la tarjeta de contacto o del panel de personas y los datos permanecen en la memoria durante más tiempo que el intervalo de actualización. Tenga en cuenta que la actualización desde la red social siempre la inicia un usuario actualizando la tarjeta de contacto o el panel de personas (por ejemplo, seleccionando un usuario diferente en el panel de personas o seleccionando un elemento diferente en la ventana del explorador de Outlook). 

Sin embargo, no siempre es cierto lo contrario, no todas las actualizaciones de la tarjeta de contacto o del panel de personas implican necesariamente una actualización desde la red social. Si el usuario actualiza la tarjeta de contacto o el panel de personas y los datos de la persona (o la actividad) permanecen en la memoria durante más tiempo que el intervalo de actualización, el OSC llama a [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) (o [ISocialSession2::GetActivitiesEx)](isocialsession2-getactivitiesex.md)para actualizar la información de la memoria de la red social. El período permitido para la información de amigos y no amigos en la memoria es de 24 horas y para actividades de 30 minutos. 
  
Una diferencia importante entre la sincronización en caché y a petición es que la sincronización a petición puede capturar información de persona y actividad para amigos y no amigos en la red. Si la persona seleccionada no es un amigo, el OSC actualiza la información y las actividades de esa persona si se cumple alguno de los siguientes requisitos: 
  
- La persona es un usuario de la red social y permite la visualización pública de la información de perfiles y actividades.
    
- La persona está en la misma red que el usuario que ha iniciado sesión en esa red social (por ejemplo, en la misma red para antiguos alumnos universitarios).
    
La sincronización a petición de personas y actividades genera más llamadas al proveedor desde el motor principal de OSC. Las redes sociales deben ser capaces de controlar los requisitos de ancho de banda aumentados de la sincronización a petición.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Especificación de elementos XML para la sincronización a petición

El proveedor de OSC informa al OSC de que admite la sincronización a petición de amigos y no amigos especificando los siguientes elementos en el XML **de funcionalidades:** 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **false**
    
- **dynamicContactsLookup**  =  **true**
    
El proveedor de OSC informa al OSC de que admite la sincronización a petición de las actividades especificando los siguientes elementos en el XML **de capacidades:** 
  
- **getActivities**  =  **true**
    
- **cacheActivities**  =  **false**
    
- **dynamicActivitiesLookupEx**  =  **true**
    
## <a name="hybrid-synchronization"></a>Sincronización híbrida

Un proveedor de OSC puede admitir la sincronización híbrida de amigos y no amigos. Esto puede optimizar las llamadas entre el motor principal de OSC y el proveedor de OSC, las llamadas a la red social para la sincronización a petición de amigos y la moneda de los datos de los amigos. El tiempo mínimo que los datos pueden permanecer en una carpeta o memoria, si procede, es el mismo que los límites en los modos de sincronización en caché o a petición.
  
> [!NOTE]
> A partir de Outlook Social Connector 2013, el OSC solo admite la sincronización a petición de actividades y ya no admite la sincronización híbrida de actividades. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Sincronización híbrida de amigos y no amigos

Si un proveedor de OSC admite la sincronización híbrida de amigos y no amigos, el OSC hace lo siguiente: 
  
- El OSC almacena información para amigos del usuario que ha iniciado sesión en la carpeta de contactos específica de la red social.
    
- El OSC almacena información para no amigos del usuario que ha iniciado sesión en la memoria.
    
El proveedor de OSC informa al OSC de que admite la sincronización híbrida de amigos y no amigos especificando los siguientes elementos en el XML **de funcionalidades:** 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **true**
    
- **dynamicContactsLookup**  =  **true**
    
## <a name="synchronization-intervals"></a>Intervalos de sincronización

En la siguiente tabla se resumen los intervalos de sincronización de la información de amigos y no amigos entre la memoria caché correspondiente (carpeta o memoria) y la red social, en función del modo de sincronización admitido. Para el modo de sincronización híbrida, consulte las filas para el modo en caché para amigos y la fila para el modo a petición para no amigos.
  
|**Modo de sincronización para personas**|**Dónde se establece el intervalo de actualización**|**Tiempo mínimo predeterminado antes de la actualización**|**Invalidación de directiva de grupo**|
|:-----|:-----|:-----|:-----|
|Cached  <br/> |Establecer en OSC  <br/> |1440 minutos (24 horas)  <br/> |Valor del Registro de Windows **NetContactSyncInterval** <br/> |
|Cached  <br/> |**Elemento contactSyncRestartInterval** en **xml de funcionalidades**  <br/> |30 minutos si **contactSyncRestartInterval** no está establecido  <br/> |Valor del Registro de Windows **contactSyncRestartInterval** <br/> |
|A petición  <br/> |Establecer en OSC  <br/> |1440 minutos (24 horas)  <br/> |Valor del Registro de Windows **OnlineSearchExpiryTime** <br/> |
   
En la siguiente tabla se resumen los intervalos de sincronización de las actividades de amigos y no amigos entre la memoria caché correspondiente (carpeta o memoria) y la red social, en función de los modos de sincronización admitidos. 
  
|**Modo de sincronización para actividades**|**Dónde se establece el intervalo de actualización**|**Tiempo mínimo predeterminado antes de la actualización**|**Invalidación de directiva de grupo**|
|:-----|:-----|:-----|:-----|
|A petición  <br/> |Establecer en OSC  <br/> |30 minutos  <br/> |Valor del Registro de Windows **OnlineSearchExpiryTime** <br/> |
   
La siguiente información se aplica a los valores del Registro de Windows enumerados en las dos tablas:
  
- Clave:  `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- Valor: valor DWORD entre 1 y 10080
    
## <a name="see-also"></a>Consulte también

- [Ejemplo xml de funcionalidades](capabilities-xml-example.md)  
- [XML para funcionalidades](xml-for-capabilities.md)
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Cómo administrar Outlook Social Connector mediante la directiva de grupo](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

