---
title: Probar a seguir y dejar de seguir a personas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: En este tema se describen escenarios para probar la capacidad del proveedor de Outlook Social Connector (OSC) de seguir a un amigo y dejar de seguir a un amigo en la red social.
ms.openlocfilehash: 06a2bc48fa723f4d4513376cace96a195cef9fa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432453"
---
# <a name="testing-following-and-stop-following-persons"></a>Probar a seguir y dejar de seguir a personas

En este tema se describen escenarios para probar la capacidad del proveedor de Outlook Social Connector (OSC) de seguir a un amigo y dejar de seguir a un amigo en la red social.
  
## <a name="following-a-person"></a>Seguir a una persona

Seguir a una persona es agregar a una persona como un amigo en la red social, usando la dirección SMTP proporcionada por el elemento de Outlook seleccionado. Seguir a alguien en una red social normalmente implica solicitar permiso a esa persona por un correo electrónico a esa dirección SMTP. Para conceder permiso, esa persona debe tener esa dirección SMTP ya incluida en su cuenta de red social o estar dispuesto a agregar ese SMTP a una cuenta de red social. Pruebe cada uno de los siguientes escenarios para comprobar que el proveedor de OSC se comporta correctamente.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Intentar seguir a una persona de la red social que existe en la red social.  <br/> |Para una red social que no requiere permiso de la persona, la red social agrega inmediatamente a la persona como un amigo.  <br/> Para una red que requiere permiso de esa persona, la red social envía una notificación. El panel de personas de Outlook muestra un icono pendiente para esa persona.  <br/> |
|Intentar seguir a una persona de la red social que no existe en la red social.  <br/> |El proveedor de OSC muestra el error adecuado en [ISocialSession::FollowPerson](isocialsession-followperson.md) o [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).  <br/> |
|Seguir a un amigo en la red social.  <br/> |Para el amigo seleccionado en el panel de personas, se muestran el distintivo de la red social y la imagen de perfil del amigo para esa red social.  <br/> |
|Seleccionar el vínculo a la página de perfil de un amigo.  <br/> |La página del amigo en la red social se abre en el explorador predeterminado del usuario que ha iniciado sesión.  <br/> |
   
## <a name="stop-following-a-person"></a>Dejar de seguir a una persona

Dejar de seguir a una persona es quitar a esa persona como un amigo en la red social. Pruebe el siguiente escenario para comprobar que el proveedor de OSC deja de seguir a una persona correctamente.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Intentar quitar a una persona como un amigo en la red social.  <br/> |La red social ya no muestra a esa persona como un amigo en la cuenta del usuario que ha iniciado sesión.  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Prepararse para publicar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md)

