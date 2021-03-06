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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435463"
---
# <a name="message-content"></a>Contenido del mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay dos codificaciones posibles para el contenido del mensaje: una con MIME y otra con uuencode. MIME es la codificación preferida. Además, MAPI define una propiedad por destinatario, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), que rige si la información de TNEF debe incluirse o no en un mensaje saliente. Por lo tanto, hay un total de cuatro formas de codificar el contenido del mensaje:
  
- MIME con TNEF
    
- MIME sin TNEF
    
- uuencode con TNEF
    
- uuencode sin TNEF
    
No se especifica cómo elegir MIME o uuencode para los mensajes salientes.
  
Las siguientes propiedades se excluyen de TNEF: **\* PR_SENDER_**, **PR_ATTACH_DATA_ \***, **PR_BODY**. Todas las demás propiedades de mensaje transmitibles se incluyen en la secuencia TNEF.
  
Las siguientes sugerencias están diseñadas para proporcionar una lista de parámetros que la implementación puede decidir cómo admitir:
  
- Si se codifica mediante MIME o uuencode para mensajes salientes: booleano.
    
- Juego de caracteres que se usará para los mensajes salientes: cadena (copiada directamente en el parámetro charset) o enumeración (traducida internamente a cadena charset).
    

