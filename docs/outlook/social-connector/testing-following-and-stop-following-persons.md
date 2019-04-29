---
title: Probar a seguir y dejar de seguir a personas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: En este tema se describen los escenarios para probar la capacidad del proveedor de Outlook Social Connector (OSC) para seguir a un amigo y dejar de seguir a un amigo en la red social.
ms.openlocfilehash: 06a2bc48fa723f4d4513376cace96a195cef9fa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432453"
---
# <a name="testing-following-and-stop-following-persons"></a>Probar a seguir y dejar de seguir a personas

En este tema se describen los escenarios para probar la capacidad del proveedor de Outlook Social Connector (OSC) para seguir a un amigo y dejar de seguir a un amigo en la red social.
  
## <a name="following-a-person"></a>Seguir a una persona

Para seguir a una persona, debe agregar una persona como amigo en la red social mediante la dirección SMTP proporcionada por el elemento seleccionado de Outlook. Seguir a alguien en una red social suele implicar solicitar permiso a esa persona mediante un correo electrónico a esa dirección SMTP. Para conceder el permiso, esa persona debe tener esa dirección SMTP ya incluida en su cuenta de red social o estar dispuesta a agregarlo a una cuenta de red social. Pruebe cada uno de los escenarios siguientes para comprobar que el proveedor de OSC se comporta correctamente.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Intentar seguir a una persona en la red social que existe en la red social.  <br/> |Para una red social que no requiera permiso de la persona, la red social agregará inmediatamente a la persona como amigo.  <br/> En el caso de una red que requiera permiso de esa persona, la red social envía una notificación. El panel de personas de Outlook muestra un icono pendiente para esa persona.  <br/> |
|Intentar seguir a una persona en la red social que no existe en la red social.  <br/> |El proveedor OSC muestra el error correspondiente en [ISocialSession:: FollowPerson](isocialsession-followperson.md) o [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md).  <br/> |
|Seguir a un amigo en la red social.  <br/> |Para el amigo seleccionado en el panel de personas, se muestra la tarjeta de identificación de la red social y la imagen de perfil del amigo para esa red social.  <br/> |
|Seleccionar el vínculo a la página de Perfil de un amigo.  <br/> |La página del amigo en la red social se abre en el explorador predeterminado del usuario que ha iniciado sesión.  <br/> |
   
## <a name="stop-following-a-person"></a>Dejar de seguir a una persona

Para dejar de seguir a una persona, debe quitar a esa persona como amigo en la red social. Pruebe el siguiente escenario para comprobar que el proveedor de OSC deje de seguir a una persona correctamente.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Intentar quitar a una persona como amigo en la red social.  <br/> |La red social ya no muestra a esa persona como amigo en la cuenta del usuario que ha iniciado sesión.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Preparación para la publicación de un proveedor OSC](getting-ready-to-release-an-osc-provider.md)

