---
title: Novedades para proveedores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92f59a0d-3834-424d-ad81-167fdeba9bd0
description: En este tema se enumeran los principales cambios en Outlook Social Connector 2013 (OSC). Presenta una comparación de las características disponibles entre Outlook Social Connector 2013 y Outlook Social Connector 1.1.
ms.openlocfilehash: 6b735555d312c149d7dc8b827990b96bfc229678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435456"
---
# <a name="whats-new-for-providers"></a>Novedades para proveedores

En este tema se enumeran los principales cambios en Outlook Social Connector 2013 (OSC). Presenta una comparación de las características disponibles entre Outlook Social Connector 2013 y Outlook Social Connector 1.1. También describe los miembros de la interfaz y los elementos XML que se han agregado, modificado o desusado. 
  
En Office 2013, el OSC funciona no solo con Outlook, sino también con SharePoint Server, SharePoint Workspace, lync client y todas las demás aplicaciones cliente de Office que admiten información de presencia y la tarjeta de contacto. Un proveedor de OSC puede  mostrar actualizaciones de información social en la pestaña NOVEDADes del panel de contactos de Outlook, así como en la tarjeta de contacto. 
  
Algunos cambios importantes en Outlook Social Connector 2013 son los siguientes: 
  
- Si un proveedor admite mostrar actividades, el proveedor siempre sincroniza las actividades a petición y ya no se basa en actividades almacenadas previamente en caché. Esto significa que el proveedor almacena actividades de amigos y no amigos en la memoria para mostrar actividades más actuales.
    
- Por motivos de seguridad, los proveedores que se comunican con servidores a través de Internet deben usar el protocolo HTTPS (Protocolo de transferencia de hipertexto (HTTP) con capa de socket seguro (SSL).. De lo contrario, existe el riesgo de que las direcciones de correo electrónico, las actividades de la red social y otros datos de usuario se intercepten o exponan mientras están en tránsito.
    
- Si tiene proveedores que trabajan con una versión anterior de Outlook, para admitir Office 2013, debe actualizar el paquete de instalación. Consulte [Lista de comprobación de](installation-checklist.md) instalación para obtener más información. 
    
En la tabla siguiente se muestra la disponibilidad de varias características en Outlook Social Connector 2013 en comparación con Outlook Social Connector 1.1.
  
|**Característica**|**Outlook Social Connector 2013**|**Outlook Social Connector 1.1**|
|:-----|:-----|:-----|
|Interfaz de usuario final  <br/> |SharePoint Servidor, SharePoint área de trabajo, cliente lync, tarjeta de contacto en todas las Office cliente y panel de personas en Outlook  <br/> |Panel de personas en Outlook  <br/> |
|Autenticación básica  <br/> |Sí  <br/> |Sí  <br/> |
|Autenticación basada en formularios  <br/> |Sí  <br/> |Sí  <br/> |
|Autenticación almacenada en caché  <br/> |Sí  <br/> |Sí  <br/> |
|Sincronización en caché de amigos a la carpeta de contactos en el almacén predeterminado  <br/> |Sí  <br/> |Sí  <br/> |
|Sincronización de actividades almacenadas en caché para amigos con **la carpeta de fuentes de noticias** ocultas  <br/> |No  <br/> |Sí  <br/> |
|Sincronización a petición (imagen, nombre, título) para amigos y no amigos en la red  <br/> |Sí  <br/> |Sí  <br/> |
|Sincronización de actividades a petición para amigos y no amigos en la red  <br/> |Sí  <br/> |Sí  <br/> |
|Seguir en red  <br/> |Sí  <br/> |Sí  <br/> |
|No seguir en la red  <br/> |Sí  <br/> |Sí  <br/> |
|Visitar página de perfil de usuario  <br/> |A través de un vínculo  <br/> |A través de un distintivo de red  <br/> |
|Observar la configuración de privacidad en la red social (por ejemplo, mostrar perfiles y actividades de no amigos que permiten la visualización de tales)  <br/> |Sí  <br/> |Sí  <br/> |
|Direcciones de correo electrónico hash pasadas al proveedor  <br/> |Sí  <br/> |Sí  <br/> |

<a name="OlSocialConnector_Changes"> </a>

## <a name="changes-from-the-previous-version-of-osc-provider-extensibility"></a>Cambios de la versión anterior de extensibilidad del proveedor de OSC

En la tabla siguiente se muestran los miembros que se han agregado o desusado de la interfaz correspondiente.
  
|**Interfaz y miembro**|**Comment**|
|:-----|:-----|
|**ISocialProfile::GetActivitiesOfFriendsAndColleagues** <br/> |En desuso Outlook Social Connector 2013. Tenga en **cuenta que ISocialSession::GetActivities** también ha quedado en desuso desde Outlook Social Connector 1.1.  <br/> Para sincronizar fuentes de actividad, debe implementar el método [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Establezca **dynamicActivitiesLookupEx** como **true**, lo que pedirá al OSC que llame a **ISocialSession2::GetActivitiesEx** en su lugar.  <br/> |
   
En la tabla siguiente se muestran los elementos de esquema que han cambiado.
  
|**Elemento Schema**|**Comment**|
|:-----|:-----|
|**capabilities** <br/> |Se agregó Outlook Social Connector 2013: **elemento allowChangesToAutoConfigure.**  <br/> En desuso Outlook elemento Social Connector 2013: **cacheActivities.**  <br/> |
|**person** <br/> |Agregado en Outlook Social Connector 2013: **askmeabout**, **businessAddress**, **businessCity**, **businessCountryOrRegion**, **businessState**, **businessZip**, **industries**, **interests**, **location**, **otherAddress**, **otherCity**, **otherCountryOrRegion**, **otherState**, **otherZip**, **skills**, **schools** y **elementos de** sitio web.  <br/> |
   
## <a name="see-also"></a>Vea también

- [XML para funcionalidades](xml-for-capabilities.md)
- [XML para amigos](xml-for-friends.md)
- [Introducción al desarrollo de un Outlook social connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

