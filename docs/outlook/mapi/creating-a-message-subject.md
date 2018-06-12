---
title: Creación de un asunto del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 419c9776b380436b1a7163803a8677fb6a89be97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816626"
---
# <a name="creating-a-message-subject"></a>Creación de un asunto del mensaje

  
  
**Se aplica a**: Outlook 
  
El asunto de un mensaje, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), es una propiedad opcional, que se usa para resumir la intención de un mensaje. Si decide establecer, convertirla en una cadena de caracteres 128 bytes o menos. El límite de 128 bytes no es un límite impuesto por MAPI; es un límite impuesto por algunos proveedores de almacén de mensajes. Para asegurar la interoperabilidad con los proveedores que se imponen, limitar sujetos a 128 bytes. 
  
Tenga en cuenta que algunos proveedores de almacén de mensajes no permitir **PR_SUBJECT** se escriban en un objeto stream con la interfaz [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) . 
  
No establezca **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Esta propiedad se establezca sólo en las respuestas y los mensajes reenviada. 
  

