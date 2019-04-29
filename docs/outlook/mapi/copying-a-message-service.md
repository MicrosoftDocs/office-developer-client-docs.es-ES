---
title: Copiar un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425396"
---
# <a name="copying-a-message-service"></a>Copiar un servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para copiar un servicio de mensajes en un perfil**
  
- Llamar a [IMsgServiceAdmin:: CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Cuando se copia un servicio de mensajes, la nueva instancia del servicio se configura exactamente de la misma manera que el original. A veces **CopyMsgService** devuelve el error MAPI_E_ACCESS_DENIED. La causa más común de esta devolución de error es un servicio de mensajes que no permite su duplicación. 
  

