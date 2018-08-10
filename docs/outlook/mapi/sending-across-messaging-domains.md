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
ms.openlocfilehash: 1fc5e4de63815c2cbfcb4818a9f6454af8c4d93b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820598"
---
# <a name="sending-across-messaging-domains"></a>Enviar a través de dominios de mensajería

  
  
**Hace referencia a**: Outlook 
  
Un dominio de mensajería representa uno o varios sistemas de mensajería que comparten un formato de dirección común. La comunicación a través de varios dominios de mensajería implica traducir un mensaje enviado en el formato del dominio de mensajería original en el formato del dominio de mensajería de destino. Debido a que no todos los formatos de dirección son compatibles, es necesario una puerta de enlace para traducir la información de hacer frente a partir del formato de origen en el formato de destino. Para garantizar la validez entre dominios de mensajería, las aplicaciones cliente de almacenan información de hacer frente a importantes en las propiedades MAPI. Además, las puertas de enlace realizan la traducción, examen de las propiedades que deben traducción y cambia a un formato que puede usar el dominio de mensajería de destino.
  
MAPI permitido anteriormente, esta información de dirección que se asociará con sólo los usuarios que conforman la lista de destinatarios actual de un mensaje. Las propiedades que describen a cada miembro de la lista de destinatarios han sufrido la conversión requerida por la puerta de enlace para garantizar la validez entre dominios de mensajería. Sin embargo, algunas aplicaciones requieren que sus mensajes de incluyen información acerca de los usuarios que quizás estaban los destinatarios en el pasado de direccionamiento, serán destinatarios en el futuro o nunca será destinatarios. Por ejemplo, aplicaciones de enrutamiento, que envían mensajes a un grupo de usuarios en un orden especificado, incluyen hacer frente a información acerca de estos usuarios en los mensajes. Normalmente, la información insertada incluye la dirección y el tipo de dirección de los destinatarios futuros y, posiblemente, también sus roles y posiciones en el orden de distribución, sus nombres y uno o varios identificadores binarios por destinatario.
  
Para permitir los mensajes incluir información acerca de estos usuarios nonrecipient, MAPI ahora incluye una estrategia para asegurarse de que esta información nonrecipient también se traduce correctamente a través de dominios de mensajería. Esta estrategia se basa en el concepto de propiedades pueda asignar la puerta de enlace.
  

