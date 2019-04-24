---
title: Asignación de atributos de correo de Internet a las propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355821"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>Asignación de atributos de correo de Internet a las propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este apéndice describe cómo un proveedor de transporte MAPI o una puerta de enlace compatible con MAPI que se conecta a Internet deben traducir entre las propiedades de los mensajes MAPI y los atributos del mensaje del Protocolo simple de transferencia de correo (SMTP). SMTP es el protocolo de mensajería que se usa en gran parte de Internet. SMTP define un conjunto de encabezados de mensaje (el sobre del mensaje) y un formato de contenido de mensaje. SMTP está completamente documentado en un conjunto de dos documentos, RFC 821 y RFC 822, que se pueden encontrar en una cantidad de sitios FTP y WWW en Internet.
  
Para obtener información sobre el protocolo SMTP que se usa para comunicarse con agentes de correo basados en SMTP, consulte RFC 821, "Protocolo simple de [https://www.rfc-editor.org](https://www.rfc-editor.org)transferencia de correo" en.
  
Para el direccionamiento y los encabezados de mensaje estándar, consulte RFC 822, "Standard para el formato de los mensajes de texto de [https://www.rfc-editor.org](https://www.rfc-editor.org)Internet arpa", en.
  
Para MIME, vea RFC 1521, "MIME (Extensiones multipropósito de correo Internet) Part One: mecanismos para especificar y describir el formato de los cuerpos de los mensajes de Internet [https://www.rfc-editor.org](https://www.rfc-editor.org), en.
  
El objetivo de asignar atributos de mensaje SMTP a las propiedades MAPI (y viceversa) es garantizar que el contenido completo de los mensajes MAPI, más allá de lo que se pueda codificar mediante atributos nativos de mensajes SMTP, se pueda intercambiar de manera confiable entre diferentes MAPI componentes que deben comunicarse a través de Internet. Este documento se basa en el trabajo ya realizado en estos componentes de Microsoft. 
  
En este documento se asume que está familiarizado con los transportes MAPI, TNEF y el correo SMTP. Se esfuerza por ser conciso en lugar de hacerlo abundantemente.
  
Como Convención, "saliente" se refiere al correo que se desplaza desde un agente de UA o MTA compatible con MAPI a Internet y "entrante" se refiere al correo que viaja desde Internet a un componente MAPI.
  

