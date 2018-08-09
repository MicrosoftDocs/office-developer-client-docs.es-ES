---
title: Probar las actividades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: Este tema describen las pruebas y escenarios para comprobar que el proveedor de Outlook Social Connector (OSC) utiliza sincronización a petición para devolver actividades de amigos y amigos que no sean de forma adecuada.
ms.openlocfilehash: 82d24b106e8d429d20a2d396eb60155cbb95f91f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821220"
---
# <a name="testing-activities"></a>Probar las actividades

Este tema describen las pruebas y escenarios para comprobar que el proveedor de Outlook Social Connector (OSC) utiliza sincronización a petición para devolver actividades de amigos y amigos que no sean de forma adecuada.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Sincronización a petición

Un proveedor de OSC implementa **ISocialProvider::GetCapabilities**, que llama a la OSC para determinar si el proveedor admite la sincronización de petición de actividades de amigos y amigos que no sean. Para las personas que se muestra en el panel de personas de Outlook, el OSC obtiene y devuelven los valores hash de su SMTP resuelve, llama a [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)y almacena (en memoria) de los datos de las actividades para estas personas. 
  
### <a name="determining-activities-to-get"></a>Determinación de las actividades para obtener

Las direcciones SMTP con algoritmo hash que se pasan a **GetActivitiesEx** son la clave para determinar si el OSC obtendrá las actividades de un amigo o que no sean de confianza. El OSC Obtiene las actividades de una persona si la persona especifica esa dirección SMTP en su cuenta de redes sociales. Si la persona no incluye esa dirección SMTP de su cuenta de red social o, si esa persona es un amigo, pero por una dirección de correo electrónico diferente de la red social, no **GetActivitiesEx** obtener las actividades de esa persona. Además, para una persona que no sea de confianza pero especifica las direcciones SMTP en su cuenta de redes sociales, los datos devueltos incluyen sólo lo que está disponible a un que no sean-amigo según lo permita la configuración de privacidad de esa persona. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Creación de temas como la prueba de amigos y amigos que no sean

Para crear a un tema de prueba para un amigo, identificar la dirección SMTP de una persona que incluye esa dirección en su cuenta de red social y que tiene un estado de confianza con el usuario ha iniciado la sesión de esa red. Crear un mensaje de correo electrónico que incluya esa dirección SMTP. De forma similar, para crear a un tema de prueba para que no sean amigo, identificar la dirección SMTP de una persona que no sea de confianza del usuario ha iniciado la sesión por esa dirección y que ha especificado en su configuración de privacidad para permitir que no sean de amigos ver sus perfiles en la red social. Crear un mensaje de correo electrónico que incluya esa dirección SMTP. 
  
En el Explorador de Outlook, cuando se selecciona el mensaje de correo electrónico que incluya un amigo (o que no son de confianza), el panel de personas muestra a los destinatarios. Selecciona la friend (o que no sean amigo) en el panel de personas permite probar que el proveedor consiste en proporcionar información acerca de la persona.
  
### <a name="test-scenarios"></a>Escenarios de prueba

Para comprobar que está recibiendo las actividades correspondientes de amigos y que no sean de amigos, pruebe los siguientes escenarios.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Persona seleccionada en el panel de personas es un amigo con el usuario ha iniciado sesión en la red social.  <br/> |El panel de personas muestra los perfiles y la imagen del perfil que las registradas en la red social de esa persona.  <br/> |
|Persona seleccionada en el panel de personas sea de confianza que no sean del usuario ha iniciado sesión en la red social, pero ha permitido su perfil puedan verse en que no sean de amigos.  <br/> |El panel de personas muestra los perfiles y la imagen del perfil que las registradas en la red social de esa persona.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md)  
- [XML de actividades](xml-for-activities.md)
- [Prepararse liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md)

