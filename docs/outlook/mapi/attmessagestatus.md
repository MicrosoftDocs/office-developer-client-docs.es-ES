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
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816475"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**Hace referencia a**: Outlook 
  
Indicadores de mensaje MAPI se asignan a marcas TNEF para preservar la compatibilidad con versiones anteriores. Todos los indicadores se agrupan juntos y codificados en un solo byte. Las asignaciones son los siguientes:
  
|**Indicadores de mensaje MAPI**|**Indicadores TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Estos marcadores se definen en el TNEF. Archivo de encabezado H.
  

