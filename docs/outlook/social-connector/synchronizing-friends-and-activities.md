---
title: Sincronizar sus amigos y actividades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: El Outlook Social Connector (OSC) admite mostrar información desde una red social acerca de una persona en la tarjeta de contacto o en el panel Outlook personas. SharePoint Servidor, SharePoint workspace, cliente lync y todas las Office cliente que admiten información de presencia admiten la tarjeta de contacto.
ms.openlocfilehash: 0d6881c5d596519422d01ca61a00b1a68e610f2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329204"
---
# <a name="synchronizing-friends-and-activities"></a>Sincronizar sus amigos y actividades

El Outlook Social Connector (OSC) admite mostrar información desde una red social acerca de una persona en la tarjeta de contacto o en el panel Outlook personas. SharePoint Servidor, SharePoint workspace, cliente lync y todas las Office cliente que admiten información de presencia admiten la tarjeta de contacto.
  
Puede usar la tarjeta de contacto en escenarios de colaboración en Office aplicaciones para obtener más información sobre las personas con las que está colaborando. Algunos ejemplos de estos escenarios incluyen la mensajería Outlook y la co-autoría de un documento en Word. Al hacer clic en la **pestaña Novedades** de una tarjeta de contacto, se muestra información sobre esa persona. 
  
El panel Outlook personas muestra información sobre una persona que puede ser remitente o destinatario de un Outlook elemento seleccionado. Siempre que seleccione otra persona en el Panel de personas u otro elemento en el explorador de Outlook o abra un elemento de Outlook en un inspector, Outlook Social Connector (OSC) actualiza el Panel de personas. 
  
Para que la tarjeta de contacto o el panel personas muestren información actual de la persona seleccionada, el OSC sincroniza dicha información a través de los proveedores de OSC y algún tipo de almacenamiento en caché. Esta sincronización depende de los proveedores de OSC instalados en el equipo cliente, las redes sociales en las que haya iniciado sesión a través de sus proveedores de OSC y el modo de sincronización que admite cada uno de los proveedores de OSC para estas redes sociales.
  
El OSC admite la sincronización de amigos, no amigos y actividades para amigos y no amigos de diferentes maneras: sincronización en caché, sincronización a petición y sincronización híbrida. La principal diferencia entre estos modos de sincronización es donde el OSC almacena los datos, ya sea en una carpeta del almacén de Outlook predeterminado del usuario o en la memoria del equipo del usuario. En cada caso, como se indica en este tema, hay un tiempo mínimo predeterminado en el que los datos permanecen en la carpeta o la memoria antes de que se actualicen los datos. En algunos casos, la directiva de grupo puede personalizar la cantidad mínima de tiempo. Para obtener más información acerca de las directivas de grupo que controlan el comportamiento del OSC, vea How [to manage the Outlook Social Connector by using Group Policy](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103).
  
Tenga en cuenta que si la persona seleccionada no es miembro de la red social, el OSC no muestra ninguna persona o información de actividad para esa persona en el Panel de personas o tarjeta de contacto.
  
## <a name="cached-synchronization"></a>Sincronización en caché

Un proveedor de OSC puede almacenar información para amigos en la red social en una carpeta específica del almacén de Outlook predeterminado del usuario y actualizar periódicamente esa memoria caché una vez transcurrido un período de tiempo especificado. Almacenar en caché información en una carpeta tiene la ventaja de reducir el tráfico a la red social.
  
> [!NOTE]
> A partir Outlook Social Connector 2013, el OSC ya no admite la sincronización en caché de actividades. 
  
### <a name="cached-synchronization-of-friends"></a>Sincronización en caché de amigos

Si un proveedor de OSC admite la sincronización en caché para amigos, el OSC almacena en caché la información de los amigos del usuario que ha iniciado sesión en la red social. La información se almacena en caché en una Outlook de contactos que es específica de esa red social en el almacén de Outlook predeterminado del usuario. El nombre de la carpeta de contactos se basa en el nombre de la red social, que el OSC obtiene mediante la propiedad [ISocialProvider::SocialNetworkName.](isocialprovider-socialnetworkname.md) 
  
En la sincronización en caché, el OSC almacena información solo para los amigos del usuario que ha iniciado sesión en la red social. El OSC no tiene acceso a la información de los que no son amigos.
  
El intervalo predeterminado para que el OSC actualice la carpeta de contactos de la información de los amigos de la red social es una vez al día (o una vez por 1440 minutos). Este intervalo de actualización también se puede establecer mediante la directiva de grupo, tal como se describe al principio de este tema.
  
Si se produce un error durante una actualización, el OSC vuelve a iniciar en un intervalo especificado por el elemento **contactSyncRestartInterval** en el XML **de funcionalidades.** Este intervalo de reintentos tiene un valor predeterminado de 30 minutos y también se puede establecer mediante directiva de grupo. 
  
Cuando un usuario abre una tarjeta  de contacto y selecciona la pestaña Novedades, **se** actualiza la pestaña Novedades. Del mismo modo, cuando un usuario Outlook vuelve a seleccionar un elemento en Outlook o vuelve a seleccionar a una persona en el Panel de personas, el panel de personas se actualiza. Si el intervalo de actualización de caché no ha expirado, el OSC va a la memoria caché para obtener información para el usuario seleccionado. Esto evita la sobrecarga de uso de la extensibilidad del proveedor de OSC para acceder a la red social. Si el intervalo de actualización ha expirado, el OSC llama al método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obtener la información de los amigos actuales del usuario que ha iniciado sesión y actualiza la memoria caché de la carpeta de contactos. 
  
El proveedor de OSC informa al OSC de que admite la sincronización en caché de amigos especificando los siguientes elementos en el XML **de funcionalidades:** 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **true**
    
- **dynamicContactsLookup**  =  **false**
    
## <a name="on-demand-synchronization"></a>Sincronización a petición

Cuando un usuario  selecciona la pestaña Novedades de una tarjeta de contacto o selecciona un elemento de Outlook diferente o una persona diferente en el Panel de personas de Outlook, el OSC actualiza la tarjeta de contacto o el panel de personas respectivamente. Si un proveedor de OSC admite la sincronización a petición de personas o actividades, el OSC se sincroniza con una memoria caché en la memoria y actualiza detalles, como el nombre, el título, la imagen y las secuencias de actividades, en el panel De contactos o personas. Para la sincronización a petición, a diferencia de la sincronización en caché, el OSC intenta actualizar la información de la persona independientemente de si esa persona es un amigo o no amigo del usuario que ha iniciado sesión en la red social. 
  
Los datos de persona a petición (o actividad) solo se almacenan en la memoria. Los datos en memoria se borran cuando la aplicación cliente de Office se apaga o el usuario provoca una actualización de la tarjeta de contacto o el panel de personas y los datos permanecen en la memoria durante más tiempo que el intervalo de actualización. Tenga en cuenta que la actualización de la red social siempre la inicia un usuario actualizando la tarjeta de contacto o el panel de personas (por ejemplo, seleccionando un usuario diferente en el panel personas o seleccionando un elemento diferente en la ventana del explorador de Outlook). 

Sin embargo, lo contrario no siempre es cierto: no todas las actualizaciones de la tarjeta de contacto o el panel de personas necesariamente incurren en una actualización de la red social. Si el usuario actualiza la tarjeta de contacto o el panel de personas y los datos de la persona (o actividad) permanecen en la memoria durante más tiempo que el intervalo de actualización, el OSC llama a [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) (o [ISocialSession2::GetActivitiesEx)](isocialsession2-getactivitiesex.md)para actualizar la información en la memoria de la red social. El período permitido para la información de amigos y no amigos en la memoria es de 24 horas y para las actividades, 30 minutos. 
  
Una diferencia importante entre la sincronización almacenada en caché y a petición es que la sincronización a petición puede capturar información de persona y actividad para amigos y no amigos en la red. Si la persona seleccionada no es un amigo, el OSC actualiza la información y las actividades de esa persona si se cumple alguno de los siguientes requisitos: 
  
- La persona es un usuario de la red social y permite la visualización pública de la información de perfil y actividad.
    
- La persona está en la misma red que el usuario que inició sesión en esa red social (por ejemplo, en la misma red para ex alumnos universitarios).
    
La sincronización a petición de personas y actividades da como resultado más llamadas al proveedor desde el motor principal de OSC. Las redes sociales deben ser capaces de controlar el aumento de los requisitos de ancho de banda de la sincronización a petición.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Especificación de elementos XML para la sincronización a petición

El proveedor de OSC informa al OSC de que admite la sincronización a petición de amigos y no amigos especificando los siguientes elementos en el XML **de funcionalidades:** 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **false**
    
- **dynamicContactsLookup**  =  **true**
    
El proveedor de OSC informa al OSC de que admite la sincronización a petición de actividades especificando los siguientes elementos en el XML **de funcionalidades:** 
  
- **getActivities**  =  **true**
    
- **cacheActivities**  =  **false**
    
- **dynamicActivitiesLookupEx**  =  **true**
    
## <a name="hybrid-synchronization"></a>Sincronización híbrida

Un proveedor de OSC puede admitir la sincronización híbrida de amigos y no amigos. Esto puede optimizar las llamadas entre el motor principal de OSC y el proveedor de OSC, las llamadas a la red social para la sincronización a petición de los amigos y la moneda de los datos de los amigos. El tiempo mínimo que los datos pueden permanecer en una carpeta o memoria, si procede, es el mismo que los límites de los modos de sincronización en caché o a petición.
  
> [!NOTE]
> A partir Outlook Social Connector 2013, el OSC solo admite la sincronización a petición de actividades y ya no admite la sincronización híbrida de actividades. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Sincronización híbrida de amigos y no amigos

Si un proveedor de OSC admite la sincronización híbrida de amigos y no amigos, el OSC hace lo siguiente: 
  
- El OSC almacena información para los amigos del usuario que ha iniciado sesión en la carpeta de contactos específica de la red social.
    
- El OSC almacena información para no amigos del usuario que ha iniciado sesión en la memoria.
    
El proveedor de OSC informa al OSC de que admite la sincronización híbrida de amigos y no amigos especificando los siguientes elementos en el XML **de funcionalidades:** 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **true**
    
- **dynamicContactsLookup**  =  **true**
    
## <a name="synchronization-intervals"></a>Intervalos de sincronización

En la tabla siguiente se resumen los intervalos de sincronización de la información de amigos y no amigos entre la memoria caché correspondiente (carpeta o memoria) y la red social, según el modo de sincronización admitido. Para el modo de sincronización híbrida, consulte las filas para el modo almacenado en caché para amigos y la fila para el modo a petición para los que no son amigos.
  
|**Modo de sincronización para personas**|**Donde se establece el intervalo de actualización**|**Tiempo mínimo predeterminado antes de la actualización**|**Invalidación de directiva de grupo**|
|:-----|:-----|:-----|:-----|
|Cached  <br/> |Establecer dentro de OSC  <br/> |1440 minutos (24 horas)  <br/> |Windows del Registro **NetContactSyncInterval** <br/> |
|Cached  <br/> |**elemento contactSyncRestartInterval** en **XML de funcionalidades**  <br/> |30 minutos si **contactSyncRestartInterval** no está establecido  <br/> |Windows valor del Registro **contactSyncRestartInterval** <br/> |
|A petición  <br/> |Establecer dentro de OSC  <br/> |1440 minutos (24 horas)  <br/> |Windows valor del Registro **OnlineSearchExpiryTime** <br/> |
   
En la tabla siguiente se resumen los intervalos de sincronización de actividades de amigos y no amigos entre la memoria caché correspondiente (carpeta o memoria) y la red social, según los modos de sincronización admitidos. 
  
|**Modo de sincronización para actividades**|**Donde se establece el intervalo de actualización**|**Tiempo mínimo predeterminado antes de la actualización**|**Invalidación de directiva de grupo**|
|:-----|:-----|:-----|:-----|
|A petición  <br/> |Establecer dentro de OSC  <br/> |30 minutos  <br/> |Windows valor del Registro **OnlineSearchExpiryTime** <br/> |
   
La siguiente información se aplica a los Windows del Registro enumerados en las dos tablas:
  
- Clave:  `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- Valor: valor DWORD entre 1 y 10080
    
## <a name="see-also"></a>Vea también

- [Ejemplo XML de funcionalidades](capabilities-xml-example.md)  
- [XML para funcionalidades](xml-for-capabilities.md)
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Cómo administrar el conector Outlook social mediante la directiva de grupo](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

