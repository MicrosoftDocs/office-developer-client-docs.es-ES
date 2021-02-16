---
title: Tipos de aplicaciones cliente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 167710243c61a7226375b88977c94ff4a517c1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417059"
---
# <a name="types-of-client-applications"></a>Tipos de aplicaciones cliente

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Existen principalmente dos tipos de clientes de mensajería: los que administran mensajes interpersonales (IPM) y los que administran los mensajes de comunicación entre procesos (IPC). Dentro de estos tipos, las aplicaciones cliente de mensajería se pueden clasificar de la siguiente manera:
  
- Persona a persona
    
- Persona a máquina
    
- Máquina a persona
    
- De máquina a máquina
    
- Combinación de personas y máquinas
    
Las aplicaciones de persona a persona implican a una persona que inicia el intercambio de mensajes y a otra persona que responde. Esta categoría de aplicaciones incluye aplicaciones de correo electrónico tradicionales, así como intercambios más estructurados, como el enrutamiento de documentos o la aprobación de gastos.
  
Las aplicaciones de persona a máquina implican a una persona que inicia el intercambio de mensajes y a una máquina que responde. Esta categoría incluye aplicaciones que usan correo electrónico para, por ejemplo, enviar una consulta de base de datos o suscribirse a una lista de distribución de correo.
  
Las aplicaciones de máquina a persona implican a una máquina que inicia el intercambio de mensajes y a una persona que responde. Esta categoría incluye aplicaciones que distribuyen documentos como fuentes de noticias y encuestas de opinión.
  
Las aplicaciones de máquina a máquina implican que una máquina inicie el intercambio de mensajes y una máquina responda. Esta categoría incluye aplicaciones como la supervisión de latidos de vínculos y la replicación de directorios y bases de datos.
  
La categoría final, una combinación de personas y máquinas, implica un escenario más complejo. Esta categoría incluye aplicaciones que no necesariamente transmiten mensajes entre remitentes y destinatarios. En su lugar, podrían publicarlas directamente en una carpeta pública o en un foro de sitio web compatible con un almacén de mensajes. A continuación, otros lectores, un administrador o un agente de software pueden consumir los mensajes a petición.
  
Si está escribiendo una aplicación de persona a persona, una aplicación de máquina a persona o una aplicación que publica mensajes en foros públicos, diseñe la aplicación para enviar y recibir mensajes IPM. Si estás escribiendo una aplicación de persona a máquina o de máquina a máquina, se puede diseñar para enviar y recibir mensajes IPC. Cualquier aplicación que requiera la interacción de un usuario humano debe admitir mensajes IPM. Las aplicaciones que implican tanto a personas como a máquinas en una variedad de escenarios a menudo deben admitir mensajes IPM e IPC. La única diferencia real entre las dos clases es que los mensajes IPM de un almacén de mensajes son visibles para los usuarios de clientes de mensajería, mientras que los mensajes IPC normalmente no son visibles para los usuarios de la aplicación cliente. 
  
En lugar de limitar los mensajes a las capacidades proporcionadas por las superclases MAPI, IPM e IPC, puede personalizar y mejorar estas clases mediante la creación de nuevas subclases IPM o IPC. La creación de subclases de mensajes implica inventar nuevas clases de mensaje que heredan de las superclases. Por ejemplo, si la aplicación de persona a persona se especializa en la administración de relaciones con el cliente, puede subclase la superclase IPM definiendo un IPM. Clase Contact.Customer y crea propiedades que describan a un cliente. Además de admitir estas propiedades personalizadas, su IPM. Los mensajes contact.customer heredarán las propiedades admitidas por todos los mensajes IPM.
  

