---
title: Crear un asunto del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395689"
---
# <a name="creating-a-message-subject"></a>Crear un asunto del mensaje

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
El asunto de un mensaje, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), es una propiedad opcional, que se usa para resumir la intención de un mensaje. Si decide establecer, convertirla en una cadena de caracteres 128 bytes o menos. El límite de 128 bytes no es un límite impuesto por MAPI; es un límite impuesto por algunos proveedores de almacén de mensajes. Para asegurar la interoperabilidad con los proveedores que se imponen, limitar sujetos a 128 bytes. 
  
Tenga en cuenta que algunos proveedores de almacén de mensajes no permitir **PR_SUBJECT** se escriban en un objeto stream con la interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . 
  
No establezca **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Esta propiedad se establezca sólo en las respuestas y los mensajes reenviada. 
  

