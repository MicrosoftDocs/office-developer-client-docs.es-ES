---
title: Probar las actividades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: En este tema se describen las pruebas y los escenarios para comprobar que el proveedor de Outlook Social Connector (OSC) usa la sincronización a petición para devolver correctamente las actividades de amigos y no amigos.
ms.openlocfilehash: 0a40dca84681a9e758c2f17d2647c339ded70462
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436303"
---
# <a name="testing-activities"></a>Probar las actividades

En este tema se describen las pruebas y los escenarios para comprobar que el proveedor de Outlook Social Connector (OSC) usa la sincronización a petición para devolver correctamente las actividades de amigos y no amigos.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Sincronización a petición

Un proveedor de OSC implementa **ISocialProvider::GetCapabilities**, al que llama el OSC para determinar si el proveedor admite la sincronización a petición de actividades de amigos y no amigos. Para las personas que se muestran en el panel de personas de Outlook, el OSC obtiene y aplica un hash a sus direcciones SMTP, llama a [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)y almacena (en la memoria) los datos de actividades devueltos para estas personas. 
  
### <a name="determining-activities-to-get"></a>Determinación de las actividades que se obtienen

Las direcciones SMTP con hash que se pasan a **GetActivitiesEx** son la clave para determinar si el OSC recibirá actividades para un amigo o no. El OSC obtiene actividades para una persona si la persona especifica esa dirección SMTP en su cuenta de red social. Si la persona no incluye esa dirección SMTP en su cuenta de red social, o si esa persona es un amigo pero por una dirección de correo electrónico diferente en la red social, **GetActivitiesEx** no obtiene actividades para esa persona. Además, para una persona que no es un amigo pero especifica las direcciones SMTP en su cuenta de red social, los datos devueltos incluyen solo lo que está disponible para un usuario que no es amigo, según lo permita la configuración de privacidad de esa persona. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Creación de temas de prueba para amigos y no amigos

Para crear un asunto de prueba para un amigo, identifique la dirección SMTP de una persona que incluya esa dirección en su cuenta de red social y que tenga un estado de amigos con el usuario que ha iniciado sesión en esa red. Cree un mensaje de correo electrónico que incluya esa dirección SMTP. De forma similar, para crear un asunto de prueba para un usuario que no sea un amigo, identifique la dirección SMTP de una persona que no sea un amigo del usuario que ha iniciado sesión por esa dirección y que haya especificado en su configuración de privacidad para permitir que los usuarios que no son amigos puedan ver su perfil en la red social. Cree un mensaje de correo electrónico que incluya esa dirección SMTP. 
  
En el explorador de Outlook, cuando selecciona el mensaje de correo electrónico que incluye un amigo (o no es un amigo), el panel de personas muestra los destinatarios. La selección del amigo (o no amigo) en el panel de personas le permite probar que el proveedor proporciona información sobre la persona.
  
### <a name="test-scenarios"></a>Escenarios de prueba

Para comprobar que estás obteniendo las actividades adecuadas para amigos y no amigos, prueba los siguientes escenarios.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|La persona seleccionada en el panel de personas es un amigo con el usuario que ha iniciado sesión en la red social.  <br/> |El panel de personas muestra el perfil y la imagen de perfil de esa persona como se publicó en la red social.  <br/> |
|La persona seleccionada en el panel de personas no es un amigo del usuario que ha iniciado sesión en la red social, pero ha permitido que su perfil sea visto por personas que no son amigos.  <br/> |El panel de personas muestra el perfil y la imagen de perfil de esa persona como se publicó en la red social.  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Sincronizar amigos y actividades](synchronizing-friends-and-activities.md)  
- [XML para actividades](xml-for-activities.md)
- [Prepararse para publicar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md)

