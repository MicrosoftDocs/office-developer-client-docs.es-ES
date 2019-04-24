---
title: Probar las actividades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98343c36-5e32-4d07-b474-adfeca693135
description: En este tema se describen las pruebas y los escenarios para comprobar que el proveedor de Outlook Social Connector (OSC) utiliza una sincronización a petición para devolver actividades de amigos y no amigos de forma adecuada.
ms.openlocfilehash: 0a40dca84681a9e758c2f17d2647c339ded70462
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329207"
---
# <a name="testing-activities"></a>Probar las actividades

En este tema se describen las pruebas y los escenarios para comprobar que el proveedor de Outlook Social Connector (OSC) utiliza una sincronización a petición para devolver actividades de amigos y no amigos de forma adecuada.

<a name="olosc_TestingActivities_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Sincronización a petición

Un proveedor OSC implementa **ISocialProvider:: GetCapabilities**, que el OSC llama para determinar si el proveedor admite la sincronización a petición de actividades de amigos y no amigos. Para las personas que se muestran en el panel de personas de Outlook, el OSC obtiene y aplica un algoritmo hash a sus direcciones SMTP, llama a [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)y almacena (en la memoria) los datos de actividades devueltos para estas personas. 
  
### <a name="determining-activities-to-get"></a>Determinación de actividades para obtener

Las direcciones SMTP con hash pasadas a **GetActivitiesEx** son la clave para determinar si el OSC recibirá actividades para un amigo o no amigo. El OSC obtiene actividades para una persona si la persona especifica esa dirección SMTP en su cuenta de red social. Si la persona no incluye esa dirección SMTP en su cuenta de red social, o si es un amigo pero tiene una dirección de correo electrónico distinta en la red social, **GetActivitiesEx** no obtiene actividades para esa persona. Además, para una persona que no es un amigo pero que especifica las direcciones SMTP en su cuenta de red social, los datos devueltos incluyen solo lo que está disponible para los usuarios que no son de confianza y que les permite la configuración de privacidad de esa persona. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Creación de asuntos de prueba para amigos y no amigos

Para crear un asunto de prueba para un amigo, identifique la dirección SMTP de una persona que incluya esa dirección en su cuenta de red social y que tenga un estado de amigo con el usuario que ha iniciado sesión en esa red. Cree un mensaje de correo electrónico que incluya la dirección SMTP. De forma similar, para crear un asunto de prueba para un servicio que no sea de confianza, identifique la dirección SMTP de una persona que no sea un amigo del usuario que ha iniciado sesión por esa dirección, y que haya especificado en su configuración de privacidad para permitir que no amigos vea su perfil en la red social. Cree un mensaje de correo electrónico que incluya la dirección SMTP. 
  
En el explorador de Outlook, cuando selecciona el mensaje de correo electrónico que incluye a un amigo (o que no es amigo), el panel de personas muestra los destinatarios. Si se selecciona el amigo (o el que no es Friend) en el panel de personas, se puede comprobar que el proveedor proporciona información sobre la persona.
  
### <a name="test-scenarios"></a>Escenarios de prueba

Para comprobar que estás obteniendo las actividades adecuadas para amigos y personas que no son amigos, prueba los siguientes escenarios.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|La persona seleccionada en el panel de personas es un amigo con el usuario que ha iniciado sesión en la red social.  <br/> |El panel de personas muestra el perfil y la imagen de Perfil de esa persona tal y como se publica en la red social.  <br/> |
|La persona seleccionada en el panel de personas no es amigo del usuario que ha iniciado sesión en la red social, pero ha permitido que su perfil sea visto por personas que no son amigos.  <br/> |El panel de personas muestra el perfil y la imagen de Perfil de esa persona tal y como se publica en la red social.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md)  
- [XML para actividades](xml-for-activities.md)
- [Preparación para la publicación de un proveedor OSC](getting-ready-to-release-an-osc-provider.md)

