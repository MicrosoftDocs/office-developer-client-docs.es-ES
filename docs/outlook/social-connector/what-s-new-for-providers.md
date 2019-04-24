---
title: Novedades para proveedores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: En este tema se enumeran los principales cambios en Outlook Social Connector 2013 (OSC). Se presenta una comparación de las características disponibles entre Outlook Social Connector 2013 y Outlook Social Connector 1,1.
ms.openlocfilehash: 6b735555d312c149d7dc8b827990b96bfc229678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329116"
---
# <a name="whats-new-for-providers"></a>Novedades para proveedores

En este tema se enumeran los principales cambios en Outlook Social Connector 2013 (OSC). Se presenta una comparación de las características disponibles entre Outlook Social Connector 2013 y Outlook Social Connector 1,1. También se describen los miembros de la interfaz y los elementos XML que se han agregado, modificado o dejado de utilizar. 
  
En Office 2013, el OSC funciona no solo con Outlook, sino también con SharePoint Server, SharePoint Workspace, cliente Lync y todas las demás aplicaciones cliente de Office que admiten información de presencia y la tarjeta de contacto. Un proveedor OSC puede exponer actualizaciones de información social en **** la pestaña novedades del panel de personas de Outlook, así como en la tarjeta de contacto. 
  
Algunos de los principales cambios en Outlook Social Connector 2013 son los siguientes: 
  
- Si un proveedor admite actividades que se muestran, el proveedor siempre sincroniza las actividades a petición y ya no se basa en las actividades previamente almacenadas en caché. Esto significa que el proveedor almacena actividades de amigos y no amigos en la memoria para mostrar actividades más actuales.
    
- Por motivos de seguridad, los proveedores que se comunican con los servidores a través de Internet deben usar el protocolo HTTPS (Protocolo de transferencia de hiperTexto (HTTP) con capa de sockets seguros (SSL)). De lo contrario, existe el riesgo de interceptar o exponer direcciones de correo electrónico, actividades de redes sociales y otros datos de usuario mientras están en tránsito.
    
- Si tiene proveedores que funcionan con una versión anterior de Outlook, para que admitan Office 2013, debe actualizar el paquete de instalación. Consulte la [lista de comprobación de instalación](installation-checklist.md) para obtener más información. 
    
En la siguiente tabla se muestra la disponibilidad de varias características en Outlook Social Connector 2013 en comparación con Outlook Social Connector 1,1.
  
|**Característica**|**Outlook Social Connector 2013**|**Outlook Social Connector 1,1**|
|:-----|:-----|:-----|
|Interfaz de usuario final  <br/> |SharePoint Server, área de trabajo de SharePoint, cliente de Lync, tarjeta de contacto en todas las aplicaciones cliente de Office y panel de personas en Outlook  <br/> |Panel de personas en Outlook  <br/> |
|Autenticación básica  <br/> |Sí  <br/> |Sí  <br/> |
|Autenticación basada en formularios  <br/> |Sí  <br/> |Sí  <br/> |
|Autenticación en caché  <br/> |Sí  <br/> |Sí  <br/> |
|Carpeta de sincronización en caché para amigos a contactos en el almacén predeterminado  <br/> |Sí  <br/> |Sí  <br/> |
|Actividades en caché sincronización de amigos a la carpeta de **suministros de noticias** ocultos  <br/> |No  <br/> |Sí  <br/> |
|Sincronización a petición (imagen, nombre, cargo) para amigos y no amigos de la red  <br/> |Sí  <br/> |Sí  <br/> |
|Actividades a petición sincronizar para amigos y no amigos en la red  <br/> |Sí  <br/> |Sí  <br/> |
|Seguir en la red  <br/> |Sí  <br/> |Sí  <br/> |
|No seguir en la red  <br/> |Sí  <br/> |Sí  <br/> |
|Página de visita de Perfil de usuario  <br/> |A través de un vínculo  <br/> |A través de un distintivo de red  <br/> |
|Observar la configuración de privacidad en la red social (por ejemplo, mostrar el perfil y las actividades de los que no son amigos y que permiten ver esto)  <br/> |Sí  <br/> |Sí  <br/> |
|Direcciones de correo electrónico con hash pasadas al proveedor  <br/> |Sí  <br/> |Sí  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Cambios de la versión anterior de la extensibilidad del proveedor OSC

En la siguiente tabla se muestran los miembros que se han agregado o desusado de la interfaz correspondiente.
  
|**Interfaz y miembro**|**Comment**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |En desuso en Outlook Social Connector 2013. Tenga en cuenta que **ISocialSession:: GetActivities** también ha quedado en desuso desde Outlook Social Connector 1,1.  <br/> Para sincronizar las fuentes de actividades, debe implementar el método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) . Establezca **dynamicActivitiesLookupEx** como **true**, lo que indicará al OSC que llame a **ISocialSession2:: GetActivitiesEx** en su lugar.  <br/> |
   
En la siguiente tabla se muestran los elementos de esquema que han cambiado.
  
|**Elemento Schema**|**Comment**|
|:-----|:-----|
|**sus** <br/> |Agregado en Outlook Social Connector 2013: elemento **allowChangesToAutoConfigure** .  <br/> En desuso en Outlook Social Connector 2013: elemento **cacheActivities** .  <br/> |
|**person** <br/> |Agregado en Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessState**, **businessZip**, **Industries**, **** interests **, Location**, **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **Skills**, **Schools**, and website Elements. ****  <br/> |
   
## <a name="see-also"></a>Vea también

- [XML para funcionalidades](xml-for-capabilities.md)
- [XML para amigos](xml-for-friends.md)
- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

