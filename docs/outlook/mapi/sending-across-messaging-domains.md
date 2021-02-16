---
title: Envío entre dominios de mensajería
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ddbaa4aeacf17f2c266ccc0ff963d005f9e403ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410115"
---
# <a name="sending-across-messaging-domains"></a>Envío entre dominios de mensajería

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un dominio de mensajería representa uno o más sistemas de mensajería que comparten un formato de dirección común. La comunicación entre varios dominios de mensajería implica traducir un mensaje enviado en el formato del dominio de mensajería original al formato del dominio de mensajería de destino. Dado que no todos los formatos de dirección son compatibles, se necesita una puerta de enlace para traducir la información de direccionamiento del formato de origen al formato de destino. Para garantizar la validez entre dominios de mensajería, las aplicaciones cliente almacenan información importante sobre el direccionamiento en las propiedades MAPI. Además, las puertas de enlace realizan la traducción, examinando las propiedades que se sabe que necesitan traducción y cambiándolos a un formato que pueda usar el dominio de mensajería de destino.
  
Anteriormente, MAPI permitía que esta información de direccionamiento se asociase solo a los usuarios que conforman la lista de destinatarios actual de un mensaje. Las propiedades que describen a cada miembro de la lista de destinatarios han pasado por debajo de la traducción requerida por la puerta de enlace para garantizar la validez en todos los dominios de mensajería. Sin embargo, algunas aplicaciones requieren que sus mensajes incluyan información de direccionamiento sobre usuarios que quizás fueron destinatarios en el pasado, serán destinatarios en el futuro o nunca serán destinatarios. Por ejemplo, las aplicaciones de enrutamiento, que envían mensajes en un orden especificado a un grupo de usuarios, insertan información de direccionamiento sobre estos usuarios en los mensajes. La información incrustada normalmente incluye la dirección y el tipo de dirección de los destinatarios futuros, y quizás también sus roles y posiciones en el orden de enrutamiento, sus nombres y uno o más identificadores binarios por destinatario.
  
Para permitir que los mensajes incluyan información sobre estos usuarios nocipientes, MAPI ahora incluye una estrategia para garantizar que esta información nocipiente también se traduzca correctamente entre dominios de mensajería. Esta estrategia se basa en el concepto de propiedades asignables a la puerta de enlace.
  

