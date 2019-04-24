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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356563"
---
# <a name="types-of-client-applications"></a>Tipos de aplicaciones cliente

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay principalmente dos tipos de clientes de mensajería: los que controlan los mensajes interpersonales (IPM) y los que administran los mensajes de comunicación entre procesos (IPC). Dentro de esos tipos, las aplicaciones cliente de mensajería se pueden clasificar de la siguiente manera:
  
- Persona a persona
    
- Persona-a-máquina
    
- Equipo a persona
    
- Equipo a equipo
    
- Combinación de personas y máquinas
    
Las aplicaciones de persona a persona implican a una persona que inicia el intercambio de mensajes y a otra persona que responde. Esta categoría de aplicaciones incluye aplicaciones de correo electrónico tradicionales, así como intercambios más estructurados, como la distribución de documentos o la aprobación de gastos.
  
Las aplicaciones de persona a máquina implican a una persona que inicia el intercambio de mensajes y un equipo que responde. Esta categoría incluye aplicaciones que usan el correo electrónico como, por ejemplo, enviar una consulta de base de datos o suscribirse a una lista de correo.
  
Las aplicaciones de equipo a persona implican un equipo que inicia el intercambio de mensajes y una persona que responde. Esta categoría incluye aplicaciones que distribuyen documentos como suministros de noticias y encuestas de opinión.
  
Las aplicaciones entre equipos implican que un equipo inicie el intercambio de mensajes y un equipo que responde. Esta categoría incluye aplicaciones como la supervisión de latido de vínculos y la replicación de directorios y bases de datos.
  
La categoría final, una combinación de personas y equipos, implica un escenario más complejo. Esta categoría incluye aplicaciones que no transmiten necesariamente mensajes entre los remitentes y los destinatarios. En su lugar, pueden publicarlos directamente en una carpeta pública o en un foro del sitio web admitido por un almacén de mensajes. Los mensajes pueden consumirse a petición por otros lectores, un administrador o un agente de software.
  
Si está escribiendo una aplicación persona a persona, aplicación de equipo a persona o una aplicación que envía mensajes a los foros públicos, diseñe la aplicación para que envíe y reciba mensajes IPM. Si está escribiendo una aplicación de una persona a otra o de equipo a equipo, puede diseñarse para enviar y recibir mensajes IPC. Cualquier aplicación que requiera la interacción de un usuario humano debe admitir mensajes IPM. Las aplicaciones que implican tanto personas como equipos en una variedad de escenarios a menudo deben admitir mensajes de IPM y IPC. La única diferencia real entre las dos clases es que los mensajes IPM de un almacén de mensajes son visibles para los usuarios de los clientes de mensajería, mientras que los mensajes IPC no suelen ser visibles para los usuarios de la aplicación cliente. 
  
En lugar de limitar los mensajes a las funciones proporcionadas por las superclases MAPI, IPM y IPC, puede personalizar y mejorar estas clases creando nuevas subclases IPM o IPC. La creación de subclases de mensaje implica la purga de nuevas clases de mensajes que heredan de las superclases. Por ejemplo, si la aplicación de persona a persona se especializa en la administración de relaciones con el cliente, puede subclaser la superclase IPM mediante la definición de una IPM. Contact. Customer (clase) y cree propiedades que describan un cliente. Además de admitir estas propiedades personalizadas, su IPM. Los mensajes de contacto. Customer heredarán las propiedades admitidas por todos los mensajes IPM.
  

