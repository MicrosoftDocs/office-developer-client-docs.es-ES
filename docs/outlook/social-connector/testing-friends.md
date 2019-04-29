---
title: Probar los amigos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: En este tema se describen las pruebas y los escenarios para comprobar que el proveedor de Outlook Social Connector (OSC) devuelve adecuadamente los datos de amigos y no amigos, cuando proceda, según el modo de sincronización que admita el proveedor.
ms.openlocfilehash: 1c97342fd5b219b15b1f58dbc065fc268f8e81d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433671"
---
# <a name="testing-friends"></a>Probar los amigos

En este tema se describen las pruebas y los escenarios para comprobar que el proveedor de Outlook Social Connector (OSC) devuelve adecuadamente los datos de amigos y no amigos, cuando proceda, según el modo de sincronización que admita el proveedor.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Sincronización en caché

Un proveedor OSC implementa [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md), que el OSC llama para determinar si el proveedor admite la sincronización en caché de los datos de los amigos. Después de llamar a [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), el OSC almacena los datos de los amigos devueltos en una carpeta de contactos específica de la red social en la tienda de Outlook predeterminada del usuario que ha iniciado sesión. El OSC también llama a [ISocialSession:: GetPerson](isocialsession-getperson.md) y [ISocialPerson:: GetPicture](isocialperson-getpicture.md) para obtener una imagen de perfil para cada amigo. 
  
### <a name="initiate-synchronization"></a>Iniciar la sincronización

Para iniciar la sincronización, puede activar y usar el botón depurar los **contactos de sincronización** en el componente de la cinta de la interfaz de usuario de Microsoft Office Fluent. Para obtener más información acerca de los botones de depuración de OSC, vea dePurar [un proveedor](debugging-a-provider.md). 
  
### <a name="test-scenarios"></a>Escenarios de prueba

Pruebe los siguientes elementos para comprobar que los datos de los amigos se almacenan correctamente en la memoria caché.
  
|**Elemento que se va a probar**|**Comportamiento esperado**|
|:-----|:-----|
|Carpeta de contactos  <br/> |La carpeta de contactos específica de la red social existe en la tienda Outlook predeterminada del usuario.  <br/> |
|Datos de amigos devueltos por **ISocialPerson:: GetFriendsAndColleagues** <br/> |Cada amigo corresponde a un contacto de la carpeta contactos específica de la red.  <br/> |
|Datos de amigos  <br/> |Los campos de contacto de cada amigo tienen los datos correctos.  <br/> |
|Imágenes de Perfil de amigos devueltas por **ISocialPerson:: GetPicture** <br/> |El elemento de contacto para cada amigo contiene la imagen de perfil.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Sincronización a petición

Un proveedor OSC implementa **ISocialProvider:: GetCapabilities**, que el OSC llama para determinar si el proveedor admite la sincronización a petición de amigos y no amigos. Para las personas que se muestran en el panel de personas de Outlook, el OSC obtiene y aplica un algoritmo hash a sus direcciones SMTP, llama a [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)y almacena (en la memoria) los datos devueltos para estas personas. 
  
### <a name="determining-friends-and-non-friends"></a>Determinación de amigos y personas que no son amigos

Las direcciones SMTP con hash pasadas a **GetPeopleDetails** son la clave para determinar si una persona es de confianza o no Friend. Si una persona no incluye esa dirección SMTP en su cuenta de red social, o incluso si es un amigo con una dirección de correo electrónico distinta en la red social, **GetPeopleDetails** sigue devolviendo a no **amigo** para esa persona como el ** friendStatus** en el parámetro _personsCollection_ . Además, para una persona que no es un amigo pero que especifica la dirección SMTP en su cuenta de red social, los datos devueltos incluyen solo lo que está disponible para los usuarios que no son de confianza y que les permite la configuración de privacidad de esa persona. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Creación de asuntos de prueba para amigos y no amigos

Para crear un asunto de prueba para un amigo, identifique la dirección SMTP de una persona que incluya esa dirección en su cuenta de red social y que tenga un estado de amigo con el usuario que ha iniciado sesión en esa red. Cree un mensaje de correo electrónico que incluya la dirección SMTP. De forma similar, para crear un asunto de prueba para un servicio que no sea de confianza, identifique la dirección SMTP de una persona que no sea una amiga del usuario que ha iniciado sesión por esa dirección, y que haya especificado en su configuración de privacidad para permitir a los usuarios que no sean amigos ver sus actividades en la redes sociales. m. Cree un mensaje de correo electrónico que incluya la dirección SMTP. 
  
En el explorador de Outlook, cuando selecciona el mensaje de correo electrónico que incluye a un amigo (o que no es amigo), el panel de personas muestra los destinatarios. Si se selecciona el amigo (o el que no es Friend) en el panel de personas, se puede comprobar que el proveedor proporciona información sobre la persona.
  
### <a name="test-scenarios"></a>Escenarios de prueba

Para comprobar que su proveedor proporciona información sobre amigos y no amigos adecuadamente, pruebe los siguientes escenarios.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|La persona seleccionada en el panel de personas es un amigo con el usuario que ha iniciado sesión en la red social.  <br/> |El panel de personas muestra las actividades de esa persona en la red social.  <br/> |
|La persona seleccionada en el panel de personas no es amigo del usuario que ha iniciado sesión en la red social, pero ha permitido que sus actividades las vean otros usuarios que no son amigos.  <br/> |El panel de personas muestra las actividades de esa persona en la red social.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Sincronización híbrida

Si un proveedor de OSC admite la sincronización híbrida de amigos y no amigos, el OSC hace lo siguiente: 
  
- El OSC almacena información para amigos del usuario que ha iniciado sesión en la carpeta de contactos de redes sociales específicas.
    
- El OSC recupera información de las personas que no son de amigos a petición desde la red social y la almacena en la memoria, pero no en una carpeta.
    
Para probar la sincronización híbrida, siga las sugerencias de prueba en la sección [sincronización en caché](#olosc_TestingFriends_CachedSync) para amigos y las que se indican en la sección [sincronización a petición](#olosc_TestingFriends_OnDemandSync) para los que no son amigos. 
  
## <a name="see-also"></a>Ver también

- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md) 
- [XML para amigos](xml-for-friends.md)
- [Preparación para la publicación de un proveedor OSC](getting-ready-to-release-an-osc-provider.md)

