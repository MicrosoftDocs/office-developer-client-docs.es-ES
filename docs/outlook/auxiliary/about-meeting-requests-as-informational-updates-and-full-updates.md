---
title: Información sobre las convocatorias de reunión como actualizaciones informativas y completas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Una solicitud de reunión es un correo electrónico que tiene IPM. Schedule.Meeting.Request como clase de mensaje. De forma predeterminada, un asistente que recibe una solicitud de reunión le responde directamente.
ms.openlocfilehash: 8e7ab7a85d3f9f7c0a67245b8d8ad27442f5c5e4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316999"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>Información sobre las convocatorias de reunión como actualizaciones informativas y completas

Una solicitud de reunión es un correo electrónico que tiene **IPM. Schedule.Meeting.Request** como clase de mensaje. De forma predeterminada, un asistente que recibe una solicitud de reunión le responde directamente. Outlook permite configurar delegados que puedan responder a solicitudes de reunión en nombre del destinatario principal. Mediante programación, Outlook la propiedad con nombre [PidLidMeetingType](https://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) de una solicitud de reunión para identificar el estado de actualización actual. 
  
## <a name="recipients-without-delegates"></a>Destinatarios sin delegados

Cuando Outlook una nueva solicitud de reunión, Outlook establece la propiedad **PidLidMeetingType** del elemento de solicitud de reunión en **mtgRequest**. Cualquier actualización posterior de esa reunión es **mtgFullUpdate** (una actualización completa) o **mtgInfoUpdate** (una actualización informativo) según la causa de la actualización, con Outlook **establecer PidLidMeetingType** en consecuencia. Una actualización completa requiere que un asistente responda explícitamente a la solicitud de reunión, y una actualización informativo no lo hace. 
  
## <a name="full-updates"></a>Actualizaciones completa

Hay dos escenarios que resultan en una actualización completa:
  
- Cuando un organizador cambia la fecha, la hora, las zonas horarias o la periodicidad de una solicitud de reunión anterior, el organizador debe enviar una actualización a todos los asistentes. Esta actualización es una actualización completa a la que un asistente debe responder explícitamente para notificar al organizador de la asistencia, ya que Outlook omite las respuestas anteriores.
    
- Si un asistente no ha respondido a una solicitud de reunión inicial y recibe una actualización posterior, la solicitud de reunión inicial queda des actualizada y la actualización es una actualización completa, independientemente de la causa de la actualización.
    
## <a name="informational-updates"></a>Actualizaciones informativos

Existen cuatro escenarios en los que Outlook genera una actualización informativo. En estos escenarios, responder a la actualización informativo es opcional.
  
- Si un organizador cambia la ubicación de una solicitud de reunión anterior, el organizador debe enviar una actualización a todos los asistentes. Si un asistente ya aceptó la solicitud de reunión inicial, el asistente recibe la actualización como una actualización informativo.
    
- Si un organizador agrega un asistente a una solicitud de reunión anterior, el organizador debe enviar la solicitud de reunión al asistente recién agregado y tiene la opción de incluir los asistentes existentes en la actualización. El asistente recién agregado recibe la solicitud de reunión como una nueva solicitud. Si el organizador decide enviar una actualización a los asistentes existentes, los asistentes reciben la actualización como una actualización informativo.
    
- Si un organizador quita un asistente de una solicitud de reunión anterior, el organizador debe enviar una actualización al asistente que se quitó de la solicitud de reunión y tiene la opción de incluir los asistentes existentes en la actualización. Los asistentes reciben la actualización como una actualización informativo.
    
- Si un organizador cambia el asunto o el cuerpo de una solicitud de reunión anterior, el organizador tiene la opción de enviar una actualización a los asistentes o simplemente guardar los cambios en la propia copia del organizador de la solicitud de reunión. Si el organizador decide enviar una actualización, los asistentes reciben la actualización como una actualización informativo.
    
## <a name="recipients-set-up-with-delegates"></a>Destinatarios configurados con delegados

Los destinatarios que deciden configurar delegados pueden hacer que los delegados respondan a las solicitudes de reunión que no estén marcadas como Privadas. De forma predeterminada, la entidad de seguridad recibe solo una copia de una solicitud de reunión o una copia de una actualización de una solicitud de reunión anterior, y los delegados siempre reciben la solicitud de reunión original o la actualización completa o informativo original. En esta configuración predeterminada, la entidad de seguridad siempre recibe actualizaciones y solicitudes de reunión delegadas; los delegados de la entidad de seguridad reciben solicitudes de reunión como nuevas solicitudes de reunión, actualizaciones completa o actualizaciones informativos, como se describe para destinatarios sin delegados en la sección "Destinatarios sin delegados".
  
De forma predeterminada, las entidades de seguridad pueden elegir responder a las solicitudes y actualizaciones de reuniones no privadas, aunque los delegados estén configurados para hacerlo en su nombre. Sin embargo, como alternativa, los administradores pueden configurar una directiva para evitar que los destinatarios principales respondan.
  

