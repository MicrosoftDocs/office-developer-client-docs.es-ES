---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430318"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las marcas de mensaje MAPI se asignan a las marcas TNEF para conservar la compatibilidad con versiones anteriores. Todas las marcas se agrupan y codifican en un único byte. Las asignaciones son las siguientes:
  
|**Marcas de mensaje MAPI**|**Marcas TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Estas marcas se definen en el TNEF. Archivo de encabezado H.
  

