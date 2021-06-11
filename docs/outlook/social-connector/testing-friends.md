---
title: Probar los amigos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: En este tema se describen pruebas y escenarios para comprobar que el proveedor de Outlook Social Connector (OSC) devuelva correctamente datos de amigos y no amigos, cuando corresponda, según el modo de sincronización admitido por el proveedor.
ms.openlocfilehash: 1c97342fd5b219b15b1f58dbc065fc268f8e81d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433671"
---
# <a name="testing-friends"></a>Probar los amigos

En este tema se describen pruebas y escenarios para comprobar que el proveedor de Outlook Social Connector (OSC) devuelva correctamente datos de amigos y no amigos, cuando corresponda, según el modo de sincronización admitido por el proveedor.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Sincronización en caché

Un proveedor de OSC implementa [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), al que llama el OSC para determinar si el proveedor admite la sincronización en caché de los datos de los amigos. Después de llamar a [ISocialPerson::GetFriendsAndColleagues,](isocialperson-getfriendsandcolleagues.md)el OSC almacena los datos de los amigos devueltos en una carpeta de contactos específica de la red social en el almacén de Outlook predeterminado del usuario que ha iniciado sesión. El OSC también llama a [ISocialSession::GetPerson](isocialsession-getperson.md) e [ISocialPerson::GetPicture](isocialperson-getpicture.md) para obtener una imagen de perfil para cada amigo. 
  
### <a name="initiate-synchronization"></a>Iniciar sincronización

Para iniciar la sincronización, puede activar y usar el botón de depuración **Sincronizar** contactos en el componente de la cinta de opciones de la Microsoft Office de usuario fluent. Para obtener más información acerca de los botones de depuración de OSC, vea [Depuración de un proveedor](debugging-a-provider.md). 
  
### <a name="test-scenarios"></a>Escenarios de prueba

Pruebe los siguientes elementos para comprobar que los datos de los amigos se almacenan en caché correctamente.
  
|**Elemento que se debe probar**|**Comportamiento esperado**|
|:-----|:-----|
|Carpeta Contactos  <br/> |La carpeta de contactos específicos de la red social existe en el almacén de contactos Outlook usuario.  <br/> |
|Datos de amigos devueltos por **ISocialPerson::GetFriendsAndColleagues** <br/> |Cada amigo corresponde a un contacto de la carpeta de contactos específica de la red.  <br/> |
|Datos de amigos  <br/> |Los campos de contacto de cada amigo tienen los datos correctos.  <br/> |
|Imágenes de perfil de amigos devueltas por **ISocialPerson::GetPicture** <br/> |El elemento de contacto de cada amigo contiene la imagen de perfil.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Sincronización a petición

Un proveedor de OSC implementa **ISocialProvider::GetCapabilities**, al que llama el OSC para determinar si el proveedor admite la sincronización a petición de amigos y no amigos. Para las personas que se muestran en el panel de personas de Outlook, el OSC obtiene y aplica hash a sus direcciones SMTP, llama a [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)y almacena (en memoria) los datos devueltos para estas personas. 
  
### <a name="determining-friends-and-non-friends"></a>Determinación de amigos y no amigos

Las direcciones SMTP hash que se pasan a **GetPeopleDetails** son la clave para determinar si una persona es un amigo o no amigo. Si una persona no incluye esa dirección SMTP en su cuenta de red social, o incluso si esa persona es un  amigo por una dirección de correo electrónico diferente en la red social, **GetPeopleDetails** aún devuelve no amigo para esa persona como **friendStatus** en el _parámetro personsCollection._ Además, para una persona que no es un amigo pero especifica la dirección SMTP en su cuenta de red social, los datos devueltos incluyen solo lo que está disponible para un no amigo según lo permitido por la configuración de privacidad de esa persona. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Creación de temas de prueba para amigos y no amigos

Para crear un asunto de prueba para un amigo, identifique la dirección SMTP de una persona que incluya esa dirección en su cuenta de red social y que tenga un estado de amigo con el usuario que inició sesión en esa red. Cree un mensaje de correo electrónico que incluya esa dirección SMTP. Del mismo modo, para crear un sujeto de prueba para un no amigo, identifique la dirección SMTP de una persona que no sea un amigo del usuario que inició sesión por esa dirección y, sin embargo, que haya especificado en su configuración de privacidad permitir que los no amigos puedan ver sus actividades en la red social. Cree un mensaje de correo electrónico que incluya esa dirección SMTP. 
  
En el Outlook, al seleccionar el mensaje de correo electrónico que incluye un amigo (o no amigo), el Panel de personas muestra los destinatarios. Seleccionar el amigo (o no amigo) en el Panel de personas le permite probar que el proveedor proporciona información sobre la persona.
  
### <a name="test-scenarios"></a>Escenarios de prueba

Para comprobar que el proveedor proporciona información sobre amigos y no amigos de forma adecuada, pruebe los siguientes escenarios.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|La persona seleccionada en el Panel de personas es un amigo con el usuario que ha iniciado sesión en la red social.  <br/> |El Panel de personas muestra las actividades de esa persona en la red social.  <br/> |
|La persona seleccionada en el Panel de personas no es un amigo del usuario que ha iniciado sesión en la red social, pero ha permitido que sus actividades sean vistas por personas que no son amigos.  <br/> |El Panel de personas muestra las actividades de esa persona en la red social.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Sincronización híbrida

Si un proveedor de OSC admite la sincronización híbrida de amigos y no amigos, el OSC hace lo siguiente: 
  
- El OSC almacena información para los amigos del usuario que ha iniciado sesión en la carpeta de contactos específica de la red social.
    
- El OSC recupera información que no es de amigos a petición de la red social y la almacena solo en la memoria, pero no en una carpeta.
    
Para probar la sincronización híbrida, siga [](#olosc_TestingFriends_CachedSync) las sugerencias de prueba [](#olosc_TestingFriends_OnDemandSync) de la sección Sincronización en caché para amigos y las de la sección Sincronización a petición para no amigos. 
  
## <a name="see-also"></a>Vea también

- [Sincronizar amigos y actividades](synchronizing-friends-and-activities.md) 
- [XML para amigos](xml-for-friends.md)
- [Prepararse para liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md)

