---
title: Acerca de las convocatorias de reunión como actualizaciones de informativas y completa
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Una convocatoria de reunión es un correo electrónico que tiene IPM. Schedule.Meeting.Request como la clase de mensaje. De forma predeterminada, un asistente recibir una convocatoria de reunión responde a ella directamente.
ms.openlocfilehash: 3565b2af03ef79d70fc9f2817c64a788f031c416
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816053"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>Acerca de las convocatorias de reunión como actualizaciones de informativas y completa

Una convocatoria de reunión es un correo electrónico que tiene **IPM. Schedule.Meeting.Request** como la clase de mensaje. De forma predeterminada, un asistente recibir una convocatoria de reunión responde a ella directamente. Outlook es compatible con la configuración de delegados que puede responder a las convocatorias de reunión en nombre del destinatario de la entidad de seguridad. Mediante programación, Outlook establece la propiedad con nombre [PidLidMeetingType](http://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) de una convocatoria de reunión para identificar el estado actual de la actualización. 
  
## <a name="recipients-without-delegates"></a>Destinatarios sin delegados

Cuando Outlook recibe una nueva convocatoria de reunión, elemento de la propiedad **PidLidMeetingType** de la convocatoria de reunión al **mtgRequest**de conjuntos de Outlook. Cualquier actualización posterior de la reunión es **mtgFullUpdate** (una actualización completa) o **mtgInfoUpdate** (una actualización informativa) dependiendo de la causa de la actualización, con Outlook configurar **PidLidMeetingType** en consecuencia. Una actualización completa requiere un asistente responder explícitamente a la convocatoria de reunión, y una información de la actualización no lo hace. 
  
## <a name="full-updates"></a>Actualizaciones completas

Hay dos escenarios que dan como resultado una actualización completa:
  
- Cuando el organizador cambia la fecha, hora, zonas horarias o periodicidad de una convocatoria de reunión anteriores, el organizador debe enviar una actualización a todos los asistentes. Esta actualización es una actualización completa a la que debe responder explícitamente un Asistente para notificar el organizador de asistencia, debido a que Outlook pasa por alto cualquier respuestas anteriores.
    
- Si un asistente no ha respondido a una convocatoria de reunión inicial y recibe una actualización posterior, la convocatoria de reunión inicial se queda obsoleta y la actualización es una actualización completa, independientemente de la causa de la actualización.
    
## <a name="informational-updates"></a>Actualizaciones de informativas

Hay cuatro situaciones en que Outlook genera una información de la actualización. En estos escenarios, responder a la información de la actualización es opcional.
  
- Si el organizador cambia la ubicación de una convocatoria de reunión anteriores, el organizador debe enviar una actualización a todos los asistentes. Si un asistente ya acepta la convocatoria de reunión inicial, el Asistente recibe la actualización como una información de la actualización.
    
- Si el organizador agrega a un asistente a una convocatoria de reunión anteriores, el organizador debe enviar la convocatoria de reunión a los asistentes recién agregado y tiene la opción de incluir a los asistentes existentes en la actualización. El Asistente recién agregada recibe la convocatoria de reunión como una nueva solicitud. Si elige el organizador enviar una actualización a los asistentes existentes, los asistentes reciben la actualización como una información de la actualización.
    
- Si el organizador quita a un asistente de una convocatoria de reunión anteriores, el organizador debe enviar una actualización a los asistentes que se ha quitado de la convocatoria de reunión y tiene una opción para incluir a los asistentes existentes en la actualización. Los asistentes reciben la actualización como una información de la actualización.
    
- Si el organizador cambia el asunto o el cuerpo de una convocatoria de reunión anteriores, el organizador tiene la opción de enviar una actualización a los asistentes o guardar los cambios a la copia del organizador de la convocatoria de reunión. Si elige el organizador enviar una actualización, los asistentes reciben la actualización como una información de la actualización.
    
## <a name="recipients-set-up-with-delegates"></a>Destinatarios configuración con delegados

Los destinatarios que elija para configurar los delegados pueden tener delegados responder a convocatorias de reunión que no se marcan como a privados. De forma predeterminada, la entidad de seguridad recibe sólo una copia de una convocatoria de reunión o una copia de una actualización de una convocatoria de reunión anteriores y los delegados reciben siempre la convocatoria de reunión original o una actualización completa o informativa original. En esta configuración predeterminada, la entidad de seguridad siempre recibe las convocatorias de reunión delegada y actualizaciones; los delegados de la entidad de seguridad reciban las convocatorias de reunión como nuevas convocatorias de reunión, las actualizaciones completas o actualizaciones informativas, tal como se describe para los destinatarios sin delegados en la sección "Destinatarios sin delegados".
  
De forma predeterminada, pueden elegir entidades de seguridad responder a las convocatorias de reunión que no sean privadas y las actualizaciones, aunque los delegados se configuran para realice en su nombre. Sin embargo, como alternativa, los administradores pueden configurar una directiva para evitar que a los destinatarios de entidad de seguridad de responder.
  

