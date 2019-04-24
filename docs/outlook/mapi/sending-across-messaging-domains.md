---
title: Enviar a través de dominios de mensajería
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ddbaa4aeacf17f2c266ccc0ff963d005f9e403ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339721"
---
# <a name="sending-across-messaging-domains"></a>Enviar a través de dominios de mensajería

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un dominio de mensajería representa uno o varios sistemas de mensajería que comparten un formato de dirección común. La comunicación entre varios dominios de mensajería implica convertir un mensaje enviado en el formato del dominio de mensajería original en el formato del dominio de mensajería de destino. Como no todos los formatos de dirección son compatibles, se necesita una puerta de enlace para traducir la información de direcciones del formato de origen al formato de destino. Para garantizar la validez en los dominios de mensajería, las aplicaciones cliente almacenan información de direccionamiento importante en las propiedades MAPI. Además, las puertas de enlace realizan la traducción, examinando las propiedades que se sabe que necesitan traducción y su modificación a un formato que el dominio de mensajería de destino puede usar.
  
Anteriormente, MAPI permitía que esta información de dirección se asociara solo a los usuarios que comprendan la lista de destinatarios actual de un mensaje. Las propiedades que describen cada miembro de la lista de destinatarios han sufrido la conversión necesaria por parte de la puerta de enlace para garantizar la validez en los dominios de mensajería. Sin embargo, algunas aplicaciones requieren que sus mensajes incluyan información sobre los usuarios que probablemente hayan sido destinatarios en el pasado, serán destinatarios en el futuro o nunca serán destinatarios. Por ejemplo, las aplicaciones de enrutamiento, que envían mensajes en un orden especificado a un grupo de usuarios, incruste la información de dirección de estos usuarios en los mensajes. La información incrustada normalmente incluye la dirección y el tipo de dirección de los futuros destinatarios, y quizás también sus roles y posiciones en el orden de enrutamiento, sus nombres y uno o varios identificadores binarios por destinatario.
  
Para permitir que los mensajes incluyan información sobre estos usuarios que no son destinatarios, MAPI ahora incluye una estrategia para garantizar que esta información que no es de destinatario también se traduzca correctamente entre los dominios de mensajería. Esta estrategia se basa en el concepto de propiedades asignables de puerta de enlace.
  

