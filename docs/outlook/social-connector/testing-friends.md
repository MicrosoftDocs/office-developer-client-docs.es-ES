---
title: Prueba de amigos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: Este tema describen las pruebas y escenarios para comprobar que el proveedor de Outlook Social Connector (OSC) adecuadamente devuelve datos de amigos y que no sean-amigos, en su caso, según el modo de sincronización admitido por el proveedor.
ms.openlocfilehash: 232977836833a9ef981ebef38c9ee243ea2dd2ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821235"
---
# <a name="testing-friends"></a>Prueba de amigos

Este tema describen las pruebas y escenarios para comprobar que el proveedor de Outlook Social Connector (OSC) adecuadamente devuelve datos de amigos y que no sean-amigos, en su caso, según el modo de sincronización admitido por el proveedor.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Sincronización de caché

Un proveedor de OSC implementa [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), que llama a la OSC para determinar si el proveedor admite la sincronización de caché de datos de amigos. Después de llamar a [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), el OSC almacena datos de los amigos devuelto en una carpeta de contactos específica a la red social en el almacén de Outlook predeterminado del usuario que ha iniciado la sesión. El OSC también llama a [ISocialSession::GetPerson](isocialsession-getperson.md) y [ISocialPerson::GetPicture](isocialperson-getpicture.md) para obtener una imagen de perfil para cada uno de ellos. 
  
### <a name="initiate-synchronization"></a>Iniciar la sincronización

Para iniciar la sincronización, puede activar y usar el botón de depuración **Sincronizar contactos** en el componente de la cinta de opciones de la interfaz de usuario Microsoft Office Fluent. Para obtener más información acerca de los botones OSC depuración, vea [Depurar un proveedor](debugging-a-provider.md). 
  
### <a name="test-scenarios"></a>Escenarios de prueba

Probar los siguientes elementos para comprobar que los datos de amigos se almacena en caché correctamente.
  
|**Elemento que se va a probar**|**Comportamiento esperado**|
|:-----|:-----|
|Carpeta de contactos  <br/> |La carpeta contactos sociales específicas de la red existe en el almacén de Outlook predeterminado del usuario.  <br/> |
|Datos de amigos devueltos por **ISocialPerson::GetFriendsAndColleagues** <br/> |Cada uno de ellos corresponde a un contacto en la carpeta de contactos específica de la red.  <br/> |
|Datos de amigos  <br/> |Campos de contacto para cada uno de ellos tienen los datos correctos.  <br/> |
|Imágenes de perfil de amigos devueltas por **ISocialPerson::GetPicture** <br/> |El elemento de contacto para cada uno de ellos contiene la imagen de perfil.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Sincronización a petición

Un proveedor de OSC implementa **ISocialProvider::GetCapabilities**, que llama a la OSC para determinar si el proveedor admite la sincronización de petición de amigos y amigos que no sean. Para las personas que se muestra en el panel de personas de Outlook, obtiene el OSC y los valores hash de su SMTP resuelve, llama a [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)y almacena (en memoria) de los datos devuelven para estas personas. 
  
### <a name="determining-friends-and-non-friends"></a>Determinación de amigos y amigos que no sean

Las direcciones SMTP con algoritmo hash que se pasan a **GetPeopleDetails** son la clave para determinar si una persona es un amigo o que no sean de confianza. Si una persona no incluye esa dirección SMTP de su cuenta de redes sociales, o incluso si esa persona es un amigo por una dirección de correo electrónico diferente de la red social, **GetPeopleDetails** devuelve aún **nonfriend** de esa persona como el ** friendStatus** en el parámetro _personsCollection_ . Además, para una persona que no sea de confianza pero especifica la dirección SMTP de su cuenta de redes sociales, los datos devueltos incluyen sólo lo que está disponible a un que no sean-amigo según lo permita la configuración de privacidad de esa persona. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Creación de temas como la prueba de amigos y amigos que no sean

Para crear a un tema de prueba para un amigo, identificar la dirección SMTP de una persona que incluye esa dirección en su cuenta de red social y que tiene un estado de confianza con el usuario ha iniciado la sesión de esa red. Crear un mensaje de correo electrónico que incluya esa dirección SMTP. De forma similar, para crear un tema de prueba para que no sean amigo, identificar la dirección SMTP de una persona que no sea de confianza del usuario ha iniciado la sesión por esa dirección, y aún que ha especificado en su configuración de privacidad para permitir que no sean de amigos ver sus actividades en la red social. k. Crear un mensaje de correo electrónico que incluya esa dirección SMTP. 
  
En el Explorador de Outlook, cuando se selecciona el mensaje de correo electrónico que incluya un amigo (o que no son de confianza), el panel de personas muestra a los destinatarios. Selecciona la friend (o que no sean amigo) en el panel de personas permite probar que el proveedor consiste en proporcionar información acerca de la persona.
  
### <a name="test-scenarios"></a>Escenarios de prueba

Para comprobar que su proveedor es proporcionar información sobre amigos y amigos que no sean correctamente, pruebe los siguientes escenarios.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Persona seleccionada en el panel de personas es un amigo con el usuario ha iniciado sesión en la red social.  <br/> |El panel de personas muestra las actividades de esa persona en la red social.  <br/> |
|Persona seleccionada en el panel de personas sea de confianza que no sean del usuario ha iniciado sesión en la red social, pero ha permitido su actividades puedan verse en que no sean de amigos.  <br/> |El panel de personas muestra las actividades de esa persona en la red social.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Sincronización de híbrido

Si un proveedor de OSC admite la sincronización de híbrido de amigos y amigos que no sean, el OSC hace lo siguiente: 
  
- El OSC almacena información de amigos del usuario que ha iniciado sesión en la carpeta de contactos específica de la red social.
    
- El OSC recupera información para que no sean de amigos y a petición de la red social y lo almacena en la memoria, pero no en una carpeta.
    
Para probar la sincronización de híbrida, siga las sugerencias de pruebas en la sección [Sincronización de caché](#olosc_TestingFriends_CachedSync) para amigos y los de la sección [Sincronización a petición](#olosc_TestingFriends_OnDemandSync) para que no sean de amigos. 
  
## <a name="see-also"></a>Ver también

- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md) 
- [XML de amigos](xml-for-friends.md)
- [Prepararse liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md)

