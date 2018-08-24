---
title: Evitar ciertos métodos al inicio
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 5d26583ad7ad3b4a200daf321a8994e302b75a79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580638"
---
# <a name="avoiding-certain-methods-at-startup"></a>Evitar ciertos métodos al inicio

 
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Para mejorar el rendimiento en tiempo de inicio, evitar llamadas siguientes:
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
La llamada a **IMAPIStatus::ValidateState** afecta al rendimiento únicamente cuando se realizan en la cola de MAPI o el subsistema MAPI. La razón por la que estos métodos ralentizar el procesamiento de inicio es porque no se completan hasta que la cola MAPI ha finalizado sus tareas de inicio. 
  
También debe evitar buscar en el almacén de mensajes en tiempo de inicio. Realizar la llamada de [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) cuando ha terminado el procesamiento de inicio. 
  

