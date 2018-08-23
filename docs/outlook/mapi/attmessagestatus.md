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
ms.openlocfilehash: 704707b34fb4532f0e60636df31edbae1a939f35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565749"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indicadores de mensaje MAPI se asignan a marcas TNEF para preservar la compatibilidad con versiones anteriores. Todos los indicadores se agrupan juntos y codificados en un solo byte. Las asignaciones son los siguientes:
  
|**Indicadores de mensaje MAPI**|**Indicadores TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Estos marcadores se definen en el TNEF. Archivo de encabezado H.
  

