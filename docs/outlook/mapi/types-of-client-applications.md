---
title: Tipos de aplicaciones de cliente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 783b8972c29b80e1005f0d55e00487dd0e2757b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572063"
---
# <a name="types-of-client-applications"></a>Tipos de aplicaciones de cliente

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Existen principalmente dos tipos de clientes de mensajería: las que controlan los mensajes interpersonales (IPM) y las que controlan los mensajes de comunicación entre procesos (IPC). Dentro de esos tipos, aplicaciones de cliente de mensajería se pueden clasificar como sigue:
  
- Persona a persona
    
- Persona-máquina
    
- Máquina a persona
    
- Equipo a equipo
    
- Combinación de las personas y equipos
    
Aplicaciones entre dos personas relacionadas con una persona que inicia el intercambio de mensajes y otra persona responder. Esta categoría de aplicaciones incluye las aplicaciones de correo electrónico tradicional, así como más intercambios estructurados, como la aprobación de gastos o enrutamiento de documentos.
  
Las aplicaciones de la persona a la máquina relacionadas con una persona que inicia el intercambio de mensajes y un equipo responder. Esta categoría incluye las aplicaciones que usan el correo electrónico para, por ejemplo, enviar una consulta de base de datos o suscribirse a una lista de correo.
  
Las aplicaciones de equipo a persona implican una máquina iniciando el intercambio de mensajes y una persona responde. Esta categoría incluye las aplicaciones que desea distribuir los documentos, como las fuentes de noticias y encuestas de opinión.
  
Las aplicaciones de equipo a equipo implican una máquina iniciando el intercambio de mensajes y un equipo responder. Esta categoría incluye aplicaciones como la replicación de supervisión y active directory y la base de datos de latido de vínculo.
  
La categoría final, una mezcla de personas y equipos, implica un escenario más complejo. Esta categoría incluye las aplicaciones que no necesariamente transmitir mensajes entre los remitentes y destinatarios. En su lugar, que es posible que envían ellos directamente en una carpeta pública o a un foro de sitio web compatible con un almacén de mensajes. A continuación, se pueden consumir los mensajes de propuestas por otros lectores, un administrador o un agente de software.
  
Si está escribiendo una aplicación de persona a persona, aplicación de la máquina a la persona o una aplicación que envía los mensajes a los foros públicos, diseñe la aplicación para enviar y recibir mensajes de IPM. Si está escribiendo una aplicación de persona a máquina o equipo a otro, se pueden diseñar para enviar y recibir mensajes IPC. Cualquier aplicación que requiere la interacción de un usuario humano debe admitir mensajes IPM. Las aplicaciones que implican personas y equipos en una variedad de escenarios a menudo deben admitir mensajes IPM y IPC. La única diferencia real entre las dos clases es que IPM mensajes en un almacén de mensajes están visibles para los usuarios de clientes de mensajería, mientras que los mensajes IPC normalmente no están visibles para los usuarios de la aplicación cliente. 
  
En lugar de limitar los mensajes a las funciones proporcionadas por la superclase MAPI, IPM y IPC, puede personalizar y mejorar estas clases mediante la creación de subclases IPM o IPC nuevo. Creación de subclases de mensaje implica crear nuevas clases de mensaje que heredan de la superclase. Por ejemplo, si la aplicación de persona a persona especializada en administración de relación de cliente, puede subclase de la superclase IPM definiendo un IPM. Denota la clase y crear propiedades que describen un cliente. Además de admitir estas propiedades personalizadas, su IPM. Denota mensajes heredará las propiedades compatibles con todos los mensajes IPM.
  

