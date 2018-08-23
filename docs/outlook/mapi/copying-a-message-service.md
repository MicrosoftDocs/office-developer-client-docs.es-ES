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
ms.openlocfilehash: 8388d14446a230b032e49ad0d614c85e79b8ece8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573722"
---
# <a name="copying-a-message-service"></a>Copiar un servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para copiar un servicio de mensajes a un perfil**
  
- Llame a [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
Cuando se copia un servicio de mensajes, la nueva instancia del servicio se configura en exactamente de la misma manera que el original. En ocasiones, **CopyMsgService** devuelve el error MAPI_E_ACCESS_DENIED. La causa más común de este error devuelto es un servicio de mensajes que no permitir que se duplican. 
  

