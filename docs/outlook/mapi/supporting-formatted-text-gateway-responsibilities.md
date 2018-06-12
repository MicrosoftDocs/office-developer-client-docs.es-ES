---
title: Compatibilidad con las responsabilidades de puerta de enlace de texto con formato
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 6d2c85aa76a372ba79e55dbf5b22024288214df6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820794"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Que admite texto con formato: Responsabilidades de puerta de enlace

  
  
**Se aplica a**: Outlook 
  
 **Para controlar el formato de texto enriquecido para los mensajes salientes, las puertas de enlace**
  
1. Recuperar sólo la propiedad de un mensaje **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) desde el almacén de mensajes. La principal ventaja de recuperación sólo la propiedad **PR_RTF_COMPRESSED** es que el texto del mensaje no es necesario que se envíen entre máquinas si existen la puerta de enlace y el almacén de mensajes en equipos diferentes. 
    
2. Generar el texto del mensaje de texto con formato ya sea mediante una llamada a la función de biblioteca RTF **HrTextFromCompressedRTFStream** o, si el mensaje se almacena localmente, **RTFSync**. El indicador RTF_SYNC_RTF_CHANGED debe establecerse en la llamada a **RTFSync**. Para obtener más información, vea [RTFSync](rtfsync.md).
    
3. Realizar modificaciones irreversibles en el texto del mensaje, como eliminarla de caracteres no admitidos. 
    
4. Asegúrese de que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) y todas las propiedades de auxilliary RTF se establecen o ausente.
    
5. Si se han realizado las modificaciones, llame al método **RTFSync** con el RTF_SYNC_RTF_CHANGED y el RTF_SYNC_BODY_CHANGED conjunto de indicadores. **RTFSync** se volverá a calcular las propiedades de auxilliary RTF desde el texto modificado. 
    
6. Realice las modificaciones en el texto del mensaje, como la inserción de los marcadores de posición de datos adjuntos y realizar las conversiones de página de código no destructiva irreversible.
    
7. Enviar el mensaje.
    
 **Para controlar el formato de texto enriquecido para los mensajes entrantes, las puertas de enlace**
  
1. Invertir las modificaciones de texto de mensaje que se han realizado directamente antes de que se envió el mensaje. 
    
2. Llamar a **RTFSync** si el mensaje contiene las propiedades de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) y **PR_RTF_COMPRESSED** . 
    
3. Actualizar el mensaje en el almacén de mensajes con la propiedad **PR_RTF_COMPRESSED** si el mensaje contiene actualizar con la propiedad **PR_BODY** sólo si está ausente **PR_RTF_COMPRESSED** . 
    
4. Descartar **PR_BODY** si el mensaje contiene esta propiedad y la **PR_RTF_COMPRESSED**.
    
Las puertas de enlace, llame a **RTFSync** para evitar transmitir el texto del mensaje y el texto con formato si se encuentra el almacén de mensajes en un equipo diferente. Si la puerta de enlace es local, puede establecer las dos propiedades y permitir que el almacén de mensajes para llevar a cabo la sincronización. 
  

