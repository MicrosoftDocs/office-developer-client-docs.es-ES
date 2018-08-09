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
ms.openlocfilehash: db327fdd239684140e4feeeb2a6045a2fcd5c410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816495"
---
# <a name="avoiding-certain-methods-at-startup"></a>Evitar ciertos métodos al inicio

 
  
**Hace referencia a**: Outlook 
  
Para mejorar el rendimiento en tiempo de inicio, evitar llamadas siguientes:
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
La llamada a **IMAPIStatus::ValidateState** afecta al rendimiento únicamente cuando se realizan en la cola de MAPI o el subsistema MAPI. La razón por la que estos métodos ralentizar el procesamiento de inicio es porque no se completan hasta que la cola MAPI ha finalizado sus tareas de inicio. 
  
También debe evitar buscar en el almacén de mensajes en tiempo de inicio. Realizar la llamada de [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) cuando ha terminado el procesamiento de inicio. 
  

