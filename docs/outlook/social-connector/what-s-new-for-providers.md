---
title: Novedades para los proveedores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: En este tema se enumera los principales cambios en Outlook Social Connector 2013 (OSC). Presenta una comparación de las características disponibles entre Outlook Social Connector 2013 y Outlook Social Connector 1.1.
ms.openlocfilehash: bdd7f7998f34a0ad096964050543f3f687bd0841
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821232"
---
# <a name="whats-new-for-providers"></a>Novedades para los proveedores

En este tema se enumera los principales cambios en Outlook Social Connector 2013 (OSC). Presenta una comparación de las características disponibles entre Outlook Social Connector 2013 y Outlook Social Connector 1.1. También se describen los miembros de interfaz y los elementos XML que se han agregado, modificados o en desuso. 
  
En Office 2013, el OSC funciona con no sólo Outlook, pero también SharePoint Server, SharePoint Workspace, cliente de Lync y todos los demás Office aplicaciones cliente compatibles con información de presencia y la tarjeta de contacto. Un proveedor de OSC puede exponer las actualizaciones de información social en la ficha **What ' s NEW** en el panel de personas de Outlook, así como en la tarjeta de contacto. 
  
Algunos cambios importantes en Outlook Social Connector 2013 incluyen lo siguiente: 
  
- Si un proveedor admite que muestra actividades, el proveedor siempre sincroniza las actividades a petición y ya no se basa en actividades previamente almacenadas en caché. Esto significa que el proveedor almacena las actividades de amigos y amigos que no sean en la memoria para mostrar las actividades más actuales.
    
- Por motivos de seguridad, los proveedores que se comunican con servidores a través de Internet deben usar el protocolo HTTPS (transferencia de hipertexto protocolo (HTTP) con la capa de sockets seguros (SSL)). De lo contrario, no hay un riesgo de que las direcciones, las actividades de redes sociales y otro usuario datos se intercepta o expuestos mientras están en tránsito de correo electrónico.
    
- Si dispone de los proveedores que funcionan con una versión anterior de Outlook, para admitir Office 2013, deberá actualizar el paquete de instalación. Para obtener más información, vea [Lista de comprobación de instalación](installation-checklist.md) . 
    
En la siguiente tabla muestra la disponibilidad de varias características de Outlook Social Connector 2013 en comparación con Outlook Social Connector 1.1.
  
|**Característica**|**Outlook Social Connector 2013**|**Outlook Social Connector 1.1**|
|:-----|:-----|:-----|
|Interfaz de usuario final  <br/> |SharePoint Server, SharePoint Workspace, cliente de Lync, tarjeta de contacto en todas las aplicaciones de cliente de Office y panel de personas en Outlook  <br/> |Panel de personas en Outlook  <br/> |
|Autenticación básica  <br/> |Sí  <br/> |Sí  <br/> |
|Autenticación basada en formularios  <br/> |Sí  <br/> |Sí  <br/> |
|Autenticación almacenada en caché  <br/> |Sí  <br/> |Sí  <br/> |
|Almacenar en caché sync para amigos a la carpeta Contactos predeterminada  <br/> |Sí  <br/> |Sí  <br/> |
|Sincronización de actividades en caché para amigos a carpeta oculta de **suministro de noticias**  <br/> |No  <br/> |Sí  <br/> |
|Sincronización a petición (imagen, nombre, título) de amigos y amigos en red  <br/> |Sí  <br/> |Sí  <br/> |
|Sincronización de actividades a petición de amigos y amigos en red  <br/> |Sí  <br/> |Sí  <br/> |
|Siga en red  <br/> |Sí  <br/> |Sí  <br/> |
|No siguen en red  <br/> |Sí  <br/> |Sí  <br/> |
|Visite la página de perfil de usuario  <br/> |A través de un vínculo  <br/> |A través de una tarjeta de red  <br/> |
|Observar la configuración de privacidad en una red social (por ejemplo, Mostrar perfiles y actividades de amigos-comunes que permiten la visualización de tales)  <br/> |Sí  <br/> |Sí  <br/> |
|Direcciones de correo electrónico con algoritmo hash que se pasan al proveedor  <br/> |Sí  <br/> |Sí  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Cambios de la versión anterior de extensibilidad de proveedor OSC

La siguiente tabla muestran a los miembros que se han agregado o en desuso desde la interfaz correspondiente.
  
|**Interfaz y el miembro**|**Comment**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |En desuso en Outlook Social Connector 2013. Tenga en cuenta que **ISocialSession::GetActivities** también ha quedado obsoleto desde Outlook Social Connector 1.1.  <br/> Para sincronizar las fuentes de actividades, debe implementar el método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Establezca **dynamicActivitiesLookupEx** como **true**, que se le pedirá el OSC para llamar a **ISocialSession2::GetActivitiesEx** en su lugar.  <br/> |
   
En la siguiente tabla se muestra los elementos de esquema que han cambiado.
  
|**Elemento de esquema**|**Comment**|
|:-----|:-----|
|**capacidades** <br/> |Agregado en Outlook Social Connector 2013: elemento de **allowChangesToAutoConfigure** .  <br/> En desuso en Outlook Social Connector 2013: elemento de **cacheActivities** .  <br/> |
|**person** <br/> |Agregado en Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessState**, **businessZip**, **sectores**, **intereses**, ** ubicación de**, elementos **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **habilidades**, **escuelas**y **sitio Web** .  <br/> |
   
## <a name="see-also"></a>Ver también

- [XML de capacidades](xml-for-capabilities.md)
- [XML de amigos](xml-for-friends.md)
- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

