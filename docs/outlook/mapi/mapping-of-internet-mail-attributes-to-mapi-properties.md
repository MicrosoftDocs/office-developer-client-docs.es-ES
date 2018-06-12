---
title: Asignación de atributos de correo de Internet a las propiedades de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 4d1bc5fc5a5e304d81ab4252a527d0e52b0d6e3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818298"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>Asignación de atributos de correo de Internet a las propiedades de MAPI

  
  
**Se aplica a**: Outlook 
  
En este apéndice se describe cómo debe traducir una puerta de enlace compatible con MAPI que se conecta a Internet o un proveedor de transporte MAPI entre las propiedades de mensaje MAPI y los atributos de mensaje de Protocolo Simple de transferencia de correo (SMTP). SMTP es el protocolo de mensajería que se usa en gran parte de Internet. SMTP define un conjunto de encabezados de mensaje: el sobre del mensaje y un formato de contenido del mensaje. SMTP está totalmente documentado en un conjunto de dos documentos, RFC 821 y RFC 822, que se encuentra en un número de sitios FTP y WWW en Internet.
  
Para obtener información sobre el protocolo SMTP utilizado para comunicar con los agentes de correo basado en SMTP, consulte RFC 821, "Simple Mail Transfer Protocol," en [http://www.rfc-editor.org](http://www.rfc-editor.org).
  
Para los encabezados de mensaje de asignación de direcciones y estándar, consulte RFC 822, "Estándar para el formato de ARPA Internet mensajes de texto," en [http://www.rfc-editor.org](http://www.rfc-editor.org).
  
Para MIME, vea RFC 1521, "MIME (Extensiones multipropósito de correo Internet) parte uno: mecanismos para especificar y que describe el formato de cuerpos de mensaje de Internet," en [http://www.rfc-editor.org](http://www.rfc-editor.org).
  
Es el objetivo de la asignación de atributos de mensaje SMTP a las propiedades de MAPI (y viceversa) para asegurarse de que el contenido completo de los mensajes MAPI, además de que se puede codificar con atributos de mensaje SMTP nativos, puede intercambiarse de forma confiable entre diferente MAPI componentes que deben comunicarse a través de Internet. Este documento se basa en el trabajo ya realizado en esos componentes en Microsoft. 
  
Este documento se da por supuesto familiaridad con los transportes MAPI, TNEF y SMTP correo. Se esfuerza por ser conciso en lugar de bastante claro.
  
Como una convención, "saliente" hace referencia al correo viajan desde una UA compatible con MAPI o MTA a Internet y "entrada" hace referencia al correo de viaje desde Internet a un componente MAPI.
  

