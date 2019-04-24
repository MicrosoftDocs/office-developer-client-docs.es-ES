---
title: Información sobre las convocatorias de reunión como actualizaciones informativas y completas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Una convocatoria de reunión es un correo electrónico que tiene IPM. Program. Meeting. request como la clase de mensaje. De forma predeterminada, un asistente que recibe una convocatoria de reunión le responde directamente.
ms.openlocfilehash: 8e7ab7a85d3f9f7c0a67245b8d8ad27442f5c5e4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316999"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>Información sobre las convocatorias de reunión como actualizaciones informativas y completas

Una convocatoria de reunión es un correo electrónico que tiene **IPM. Program. Meeting. request** como la clase de mensaje. De forma predeterminada, un asistente que recibe una convocatoria de reunión le responde directamente. Outlook admite la configuración de delegados que pueden responder a convocatorias de reunión en nombre del destinatario de la entidad de seguridad. Mediante programación, Outlook establece la propiedad con nombre [PidLidMeetingType](https://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) de una convocatoria de reunión para identificar el estado de actualización actual. 
  
## <a name="recipients-without-delegates"></a>Destinatarios sin delegados

Cuando Outlook recibe una nueva convocatoria de reunión, Outlook establece la propiedad **PidLidMeetingType** del elemento de convocatoria de reunión en **mtgRequest**. Cualquier actualización posterior de esa reunión es **mtgFullUpdate** (una actualización completa) o **mtgInfoUpdate** (una actualización informativa) según la causa de la actualización, con la configuración de Outlook **PidLidMeetingType** en consecuencia. Una actualización completa requiere que un asistente responda de forma explícita a la convocatoria de reunión y que la actualización informativa no. 
  
## <a name="full-updates"></a>Actualizaciones completas

Hay dos escenarios que resultan en una actualización completa:
  
- Cuando un organizador cambia la fecha, la hora, las zonas horarias o la periodicidad de una convocatoria de reunión anterior, el organizador debe enviar una actualización a todos los asistentes. Esta actualización es una actualización completa a la que un asistente debe responder expresamente para notificar al organizador la asistencia, ya que Outlook pasa por alto las respuestas anteriores.
    
- Si un asistente no respondió a una convocatoria de reunión inicial y recibe una actualización posterior, la convocatoria de reunión inicial quedará obsoleta y la actualización será una actualización completa, independientemente de la causa de la actualización.
    
## <a name="informational-updates"></a>Actualizaciones inFormativas

Hay cuatro escenarios en los que Outlook genera una actualización informativa. En estos escenarios, responder a la actualización informativa es opcional.
  
- Si un organizador cambia la ubicación de una convocatoria de reunión anterior, el organizador debe enviar una actualización a todos los asistentes. Si un asistente ya aceptó la convocatoria de reunión inicial, el asistente recibirá la actualización como una actualización informativa.
    
- Si un organizador agrega un asistente a una convocatoria de reunión anterior, el organizador debe enviar la convocatoria de reunión al asistente recién agregado y tiene la opción de incluir a los asistentes existentes en la actualización. El asistente recién agregado recibe la convocatoria de reunión como una nueva solicitud. Si el organizador elige enviar una actualización a los asistentes existentes, los asistentes recibirán la actualización como una actualización informativa.
    
- Si un organizador quita un asistente de una convocatoria de reunión anterior, el organizador debe enviar una actualización al asistente que se quitó de la convocatoria de reunión y tiene una opción para incluir a los asistentes existentes en la actualización. Los asistentes reciben la actualización como una actualización informativa.
    
- Si un organizador cambia el asunto o el cuerpo de una convocatoria de reunión anterior, el organizador tiene la opción de enviar una actualización a los asistentes o simplemente guardar los cambios en la copia del organizador de la convocatoria de reunión. Si el organizador elige enviar una actualización, los asistentes reciben la actualización como una actualización informativa.
    
## <a name="recipients-set-up-with-delegates"></a>Destinatarios configurados con delegados

Los destinatarios que decidan configurar delegados pueden hacer que los delegados respondan a las convocatorias de reunión que no se marcan como privadas. De forma predeterminada, la entidad de seguridad recibe sólo una copia de una convocatoria de reunión o una copia de una actualización a una convocatoria de reunión anterior, y los delegados siempre reciben la convocatoria de reunión original o la actualización de información original o completa. En esta configuración predeterminada, el principal siempre recibe las convocatorias de reunión y las actualizaciones delegadas; los delegados de la entidad de seguridad reciben las convocatorias de reunión como nuevas convocatorias de reunión, actualizaciones completas o actualizaciones informativas, como se describe para los destinatarios sin delegados en la sección "destinatarios sin delegados".
  
De forma predeterminada, las entidades de seguridad pueden elegir responder a las convocatorias de reunión no privadas y actualizaciones, aunque los delegados estén configurados para hacerlo en su nombre. Sin embargo, como alternativa, los administradores pueden configurar una directiva para impedir que los destinatarios principales respondan.
  

