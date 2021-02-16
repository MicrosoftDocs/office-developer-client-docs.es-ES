---
title: Asignación de atributos de correo de Internet a propiedades MAPI
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
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>Asignación de atributos de correo de Internet a propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este apéndice se describe cómo un proveedor de transporte MAPI o una puerta de enlace compatible con MAPI que se conecta a Internet debe traducir entre las propiedades de los mensajes MAPI y los atributos de mensaje del Protocolo simple de transporte de correo (SMTP). SMTP es el protocolo de mensajería que se usa en gran parte de Internet. SMTP define un conjunto de encabezados de mensaje (el sobre del mensaje) y un formato de contenido de mensaje. SMTP está completamente documentado en un conjunto de dos documentos, RFC 821 y RFC 822, que se pueden encontrar en varios sitios FTP y WWW en Internet.
  
Para obtener información sobre el protocolo SMTP usado para comunicarse con agentes de correo basados en SMTP, consulte RFC 821, "Protocolo simple de transferencia de correo", en [https://www.rfc-editor.org](https://www.rfc-editor.org) .
  
Para el direccionamiento y los encabezados de mensajes estándar, consulte RFC 822, "Estándar para el formato de mensajes de texto de Internet ARPA", en [https://www.rfc-editor.org](https://www.rfc-editor.org) .
  
Para MIME, consulte RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies", en [https://www.rfc-editor.org](https://www.rfc-editor.org) .
  
El objetivo de asignar atributos de mensaje SMTP a propiedades MAPI (y viceversa) es garantizar que el contenido completo de los mensajes MAPI, más allá de lo que se puede codificar mediante atributos de mensaje SMTP nativos, se pueda intercambiar de forma confiable entre diferentes componentes MAPI que deben comunicarse a través de Internet. Este documento se basa en el trabajo ya realizado en estos componentes en Microsoft. 
  
En este documento se supone que está familiarizado con los transportes MAPI, TNEF y correo SMTP. Se esfuerza por ser conciso en lugar de claramente clara.
  
Como convención, "saliente" hace referencia al correo que se desplaza desde un UA o MTA compatible con MAPI a Internet, y "entrante" hace referencia al correo que se desplaza desde Internet a un componente MAPI.
  

