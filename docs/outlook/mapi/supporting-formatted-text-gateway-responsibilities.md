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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327422"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Compatibilidad con texto con formato: responsabilidades de puerta de enlace

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para controlar el formato de texto enriquecido para los mensajes salientes, puertas de enlace**
  
1. Recupere solo la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) de un mensaje del almacén de mensajes. La ventaja principal de recuperar solo la propiedad **PR_RTF_COMPRESSED** es que no es necesario enviar el texto del mensaje entre equipos si la puerta de enlace y el almacén de mensajes existen en diferentes equipos. 
    
2. Genere el texto del mensaje desde el texto con formato mediante una llamada a la función de la biblioteca RTF **HrTextFromCompressedRTFStream** o, si el mensaje se almacena de forma local, **RTFSync**. La marca RTF_SYNC_RTF_CHANGED debe establecerse en la llamada a **RTFSync**. Para obtener más información, vea [RTFSync](rtfsync.md).
    
3. Realice las modificaciones irreversibles en el texto del mensaje, como la colocación de caracteres no admitidos. 
    
4. Asegúrese de que tanto **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) como todas las propiedades de auxilliary RTF estén configuradas o ausentes.
    
5. Si se han realizado modificaciones, llame a **RTFSync** con los indicadores RTF_SYNC_RTF_CHANGED y RTF_SYNC_BODY_CHANGED establecidos. **RTFSync** recalculará las propiedades de auxilliary RTF a partir del texto modificado. 
    
6. Realice las modificaciones que se puedan revertir en el texto del mensaje, como la inserción de los marcadores de posición de los datos adjuntos y la realización de conversiones de página de código no destructiva.
    
7. Enviar el mensaje.
    
 **Para controlar el formato de texto enriquecido para los mensajes entrantes, puertas de enlace**
  
1. ReVierta cualquier modificación del texto del mensaje que se haya realizado directamente antes de enviar el mensaje. 
    
2. Llame a **RTFSync** si el mensaje contiene las propiedades **PR_RTF_COMPRESSED** y **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). 
    
3. Actualizar el mensaje en el almacén de mensajes con la propiedad **PR_RTF_COMPRESSED** si el mensaje lo contiene; actualice con la propiedad **PR_BODY** solo si **PR_RTF_COMPRESSED** está ausente. 
    
4. DesCartar **PR_BODY** si el mensaje contiene esta propiedad y **PR_RTF_COMPRESSED**.
    
Las puertas de enlace llaman a **RTFSync** para evitar transmitir el texto del mensaje y el texto con formato si el almacén de mensajes se encuentra en un equipo diferente. Si la puerta de enlace es local, puede establecer ambas propiedades y permitir que el almacén de mensajes realice la sincronización. 
  

