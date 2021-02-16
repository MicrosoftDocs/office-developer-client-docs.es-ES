---
title: Novedades para proveedores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: En este tema se enumeran los cambios principales en Outlook Social Connector 2013 (OSC). Presenta una comparación de las características disponibles entre Outlook Social Connector 2013 y Outlook Social Connector 1.1.
ms.openlocfilehash: 6b735555d312c149d7dc8b827990b96bfc229678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435456"
---
# <a name="whats-new-for-providers"></a>Novedades para proveedores

En este tema se enumeran los cambios principales en Outlook Social Connector 2013 (OSC). Presenta una comparación de las características disponibles entre Outlook Social Connector 2013 y Outlook Social Connector 1.1. También describe los miembros de la interfaz y los elementos XML que se han agregado, cambiado o desusado. 
  
En Office 2013, el OSC funciona no solo con Outlook, sino también con SharePoint Server, SharePoint Workspace, el cliente lync y todas las demás aplicaciones cliente de Office que admiten la información de presencia y la tarjeta de contacto. Un proveedor de OSC puede  mostrar actualizaciones de información social en la pestaña NOVEDADes del panel de personas de Outlook, así como en la tarjeta de contacto. 
  
Entre los cambios principales en Outlook Social Connector 2013 se incluyen los siguientes: 
  
- Si un proveedor admite la presentación de actividades, este siempre sincroniza las actividades a petición y ya no se basa en las actividades almacenadas previamente en caché. Esto significa que el proveedor almacena actividades de amigos y no amigos en la memoria para mostrar actividades más actuales.
    
- Por motivos de seguridad, los proveedores que se comunican con servidores a través de Internet deben usar el protocolo HTTPS (Protocolo de transferencia de hipertexto (HTTP) con Capa de sockets seguros (SSL).. De lo contrario, existe el riesgo de que las direcciones de correo electrónico, las actividades de la red social y otros datos de usuario se intercepten o exponan mientras están en tránsito.
    
- Si tiene proveedores que trabajan con una versión anterior de Outlook, para admitir Office 2013, debe actualizar el paquete de instalación. Vea [la lista de comprobación de](installation-checklist.md) instalación para obtener más información. 
    
En la tabla siguiente se muestra la disponibilidad de varias características en Outlook Social Connector 2013 en comparación con Outlook Social Connector 1.1.
  
|**Característica**|**Outlook Social Connector 2013**|**Outlook Social Connector 1.1**|
|:-----|:-----|:-----|
|Interfaz de usuario final  <br/> |SharePoint Server, SharePoint Workspace, cliente lync, tarjeta de contacto en todas las aplicaciones cliente de Office y panel de personas en Outlook  <br/> |Panel de personas en Outlook  <br/> |
|Autenticación básica  <br/> |Sí  <br/> |Sí  <br/> |
|Autenticación basada en formularios  <br/> |Sí  <br/> |Sí  <br/> |
|Autenticación almacenada en caché  <br/> |Sí  <br/> |Sí  <br/> |
|Sincronización en caché para amigos y carpeta de contactos en el almacén predeterminado  <br/> |Sí  <br/> |Sí  <br/> |
|Sincronización de actividades almacenadas en caché para amigos en la **carpeta de fuentes de noticias** ocultas  <br/> |No  <br/> |Sí  <br/> |
|Sincronización a petición (imagen, nombre, título) para amigos y no amigos en la red  <br/> |Sí  <br/> |Sí  <br/> |
|Las actividades a petición se sincronizan para amigos y no amigos en la red  <br/> |Sí  <br/> |Sí  <br/> |
|Seguir en la red  <br/> |Sí  <br/> |Sí  <br/> |
|No seguir en la red  <br/> |Sí  <br/> |Sí  <br/> |
|Visitar página de perfil de usuario  <br/> |A través de un vínculo  <br/> |A través de un distintivo de red  <br/> |
|Observar la configuración de privacidad en la red social (por ejemplo, mostrar el perfil y las actividades de no amigos que permiten su visualización)  <br/> |Sí  <br/> |Sí  <br/> |
|Direcciones de correo electrónico con hash pasadas al proveedor  <br/> |Sí  <br/> |Sí  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Cambios de la versión anterior de la extensibilidad del proveedor de OSC

En la tabla siguiente se muestran los miembros que se han agregado o dejado de usar desde la interfaz correspondiente.
  
|**Interfaz y miembro**|**Comment**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |En desuso en Outlook Social Connector 2013. Tenga en **cuenta que ISocialSession::GetActivities** también está en desuso desde Outlook Social Connector 1.1.  <br/> Para sincronizar fuentes de actividad, debe implementar el método [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Establezca **dynamicActivitiesLookupEx** como **true**, lo que pedirá al OSC que llame a **ISocialSession2::GetActivitiesEx** en su lugar.  <br/> |
   
En la tabla siguiente se muestran los elementos de esquema que han cambiado.
  
|**Elemento Schema**|**Comment**|
|:-----|:-----|
|**capabilities** <br/> |Se agregó en Outlook Social Connector 2013: **elemento allowChangesToAutoConfigure.**  <br/> En desuso en Outlook Social Connector 2013: **elemento cacheActivities.**  <br/> |
|**person** <br/> |Agregado en Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, businessState , **businessZip**, **industries**, **interests**, **location**, **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **skills**, **schools** y **elementos de sitio web.**   <br/> |
   
## <a name="see-also"></a>Consulte también

- [XML para funcionalidades](xml-for-capabilities.md)
- [XML para amigos](xml-for-friends.md)
- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

