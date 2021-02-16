---
title: Compatibilidad con responsabilidades de puerta de enlace de texto con formato
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419432"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Texto con formato de apoyo: responsabilidades de la puerta de enlace

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para controlar el formato de texto enriquecido para los mensajes salientes, puertas de enlace**
  
1. Recupere sólo la propiedad **de** PR_RTF_COMPRESSED de un mensaje ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) del almacén de mensajes. La principal ventaja de recuperar solo la propiedad **PR_RTF_COMPRESSED** es que no es necesario enviar el texto del mensaje entre equipos si la puerta de enlace y el almacén de mensajes existen en equipos diferentes. 
    
2. Genere el texto del mensaje a partir del texto con formato llamando a la función de biblioteca RTF **HrTextFromCompressedRTFStream** o, si el mensaje se almacena localmente, **RTFSync**. La RTF_SYNC_RTF_CHANGED debe establecerse en la llamada a **RTFSync**. Para obtener más información, vea [RTFSync](rtfsync.md).
    
3. Realice modificaciones irreversibles en el texto del mensaje, como colocar caracteres no admitidos. 
    
4. Asegúrese de que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) y todas las propiedades auxiliares RTF estén establecidas o ausentes.
    
5. Si se realizaron modificaciones, llame a **RTFSync** con las marcas RTF_SYNC_RTF_CHANGED y RTF_SYNC_BODY_CHANGED establecidas. **RTFSync** recalculará las propiedades rtf auxiliares del texto modificado. 
    
6. Realice modificaciones invertibles en el texto del mensaje, como insertar marcadores de posición de datos adjuntos y realizar conversiones de páginas de códigos no destructivas.
    
7. Envíe el mensaje.
    
 **Para controlar el formato de texto enriquecido para los mensajes entrantes, puertas de enlace**
  
1. Revierta las modificaciones de texto del mensaje que se realizaron directamente antes de que se enviara el mensaje. 
    
2. Llame **a RTFSync** si el mensaje contiene las **propiedades PR_RTF_COMPRESSED** y **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). 
    
3. Actualice el mensaje en el almacén de mensajes con **la PR_RTF_COMPRESSED** propiedad si el mensaje lo contiene; actualizar con la **propiedad PR_BODY** solo **si PR_RTF_COMPRESSED** está ausente. 
    
4. Descartar **PR_BODY** si el mensaje contiene esta propiedad y **PR_RTF_COMPRESSED**.
    
Las puertas de enlace llaman a **RTFSync** para evitar transmitir el texto del mensaje y el texto con formato si el almacén de mensajes está en un equipo diferente. Si la puerta de enlace es local, puede establecer ambas propiedades y permitir que el almacén de mensajes realice la sincronización. 
  

