---
title: Contenido del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 5e8debcd5a60357f05dfb7b6bde1faf972e50a26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818387"
---
# <a name="message-content"></a>Contenido del mensaje

  
  
**Se aplica a**: Outlook 
  
Hay dos codificaciones posibles para el contenido del mensaje: uno mediante MIME, la otra mediante uuencode. MIME es la codificación preferida. Además, MAPI define una propiedad por destinatario, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), que controla si se debe incluir la información de TNEF en un mensaje saliente. Por tanto, hay un total de cuatro maneras de codificar el contenido de mensaje:
  
- MIME con TNEF
    
- MIME sin TNEF
    
- UUENCODE con TNEF
    
- UUENCODE sin TNEF
    
No se especifica cómo elegir MIME o uuencode para mensajes salientes.
  
Las siguientes propiedades se excluyen de TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**. Todas las demás propiedades de mensaje transmisible se incluyen en la secuencia TNEF.
  
Las siguientes sugerencias están diseñadas para proporcionar una lista de parámetros que la implementación puede decidir cómo se admite:
  
- Si se va a codificar con MIME o uuencode para mensajes salientes: boolean.
    
- Conjunto que se usará para los mensajes salientes de caracteres: cadena (copiados directamente al parámetro charset) o enumeración (traducido internamente en cadena de juego de caracteres).
    

