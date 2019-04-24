---
title: Contenido del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357004"
---
# <a name="message-content"></a>Contenido del mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay dos posibles codificaciones para el contenido del mensaje: uno con MIME, el otro con uuencode. MIME es la codificación preferida. Además, MAPI define una propiedad por destinatario, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), que controla si se debe incluir la información de TNEF en un mensaje saliente. Por lo tanto, hay un total de cuatro formas de codificar el contenido del mensaje:
  
- MIME con TNEF
    
- MIME sin TNEF
    
- uuencode con TNEF
    
- uuencode sin TNEF
    
No se ha especificado el modo de elegir MIME o uuencode para los mensajes salientes.
  
Las siguientes propiedades se excluyen de TNEF **:\*PR_SENDER_**, **PR_ATTACH_DATA_\***, **PR_BODY**. El resto de las propiedades de los mensajes transmitibles se incluyen en la secuencia TNEF.
  
Las siguientes sugerencias tienen como objetivo proporcionar una lista de parámetros que la implementación puede usar para decidir cómo:
  
- Si se va a codificar mediante MIME o uuencode para los mensajes salientes: Boolean.
    
- Juego de caracteres que se va a usar para los mensajes salientes: String (que se copia directamente al parámetro charset) o enumeración (se traduce internamente a la cadena del juego de caracteres).
    

