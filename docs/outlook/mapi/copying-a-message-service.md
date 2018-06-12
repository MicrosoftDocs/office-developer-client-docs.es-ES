---
title: Copiar un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 7d1296ba74bbafcd26a8878dfb1eb2f359ab3e03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816562"
---
# <a name="copying-a-message-service"></a>Copiar un servicio de mensajes

  
  
**Se aplica a**: Outlook 
  
 **Para copiar un servicio de mensajes a un perfil**
  
- Llame a [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Cuando se copia un servicio de mensajes, la nueva instancia del servicio se configura en exactamente de la misma manera que el original. En ocasiones, **CopyMsgService** devuelve el error MAPI_E_ACCESS_DENIED. La causa más común de este error devuelto es un servicio de mensajes que no permitir que se duplican. 
  

