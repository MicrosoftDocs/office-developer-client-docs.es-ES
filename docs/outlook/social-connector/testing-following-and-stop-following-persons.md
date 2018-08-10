---
title: Probar a seguir y dejar de seguir a personas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: En este tema se describe escenarios para comprobar la capacidad de un proveedor de Outlook Social Connector (OSC) que se deben seguir a un amigo y para detener el seguimiento de un amigo en la red social.
ms.openlocfilehash: 09652b658a2c20301b8b0568d373ae6fe841fe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821209"
---
# <a name="testing-following-and-stop-following-persons"></a>Probar a seguir y dejar de seguir a personas

En este tema se describe escenarios para comprobar la capacidad de un proveedor de Outlook Social Connector (OSC) que se deben seguir a un amigo y para detener el seguimiento de un amigo en la red social.
  
## <a name="following-a-person"></a>Seguimiento de una persona

Para seguir a una persona es agregar a una persona como amigo en la red social, utilizando la dirección SMTP proporcionada por el elemento seleccionado de Outlook. Seguimiento de una persona en una red social normalmente implica que se solicita el permiso de esa persona por un correo electrónico a esa dirección SMTP. Para poder conceder permiso, esa persona debe tener esa dirección SMTP ya incluida en su cuenta de redes sociales, o ser dispuesto a agregar que SMTP a una cuenta de redes sociales. Pruebe cada uno de los siguientes escenarios para comprobar que su proveedor de OSC se comporta correctamente.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Si se intenta seguir a una persona en la red social que existe en la red social.  <br/> |Para una red social que no requiere el permiso de la persona, la red social agrega inmediatamente a la persona como amigo.  <br/> Para una red que requiere el permiso de esa persona, la red social envía una notificación. El panel de personas de Outlook muestra un icono pendiente de esa persona.  <br/> |
|Si se intenta seguir a una persona en la red social que no existe en la red social.  <br/> |El proveedor de OSC muestra el error correspondiente en [ISocialSession::FollowPerson](isocialsession-followperson.md) o [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).  <br/> |
|Seguimiento de un amigo en la red social.  <br/> |Para el amigo seleccionado en el panel de personas, se muestran tarjeta de identificación de la red social y la imagen del perfil de amigo para esa red social.  <br/> |
|Al seleccionar el vínculo a la página de perfil de un amigo.  <br/> |Página de amigo en la red social se abre en el explorador predeterminado del usuario que ha iniciado la sesión.  <br/> |
   
## <a name="stop-following-a-person"></a>Detener el seguimiento de una persona

Para detener el seguimiento de una persona es quitar a esa persona como amigo en la red social. Probar el escenario siguiente para comprobar el deja de proveedor OSC siguiendo una persona correctamente.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Si se intenta quitar a una persona como amigo en la red social.  <br/> |La red social ya no muestra a esa persona como amigo en la cuenta de usuario ha iniciado la sesión.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Prepararse liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md)

