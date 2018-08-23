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
ms.openlocfilehash: cae255b90e8f2ccaaec4736c7ba1e9d6b7764f58
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593112"
---
# <a name="creating-a-message-subject"></a>Crear un asunto del mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El asunto de un mensaje, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), es una propiedad opcional, que se usa para resumir la intención de un mensaje. Si decide establecer, convertirla en una cadena de caracteres 128 bytes o menos. El límite de 128 bytes no es un límite impuesto por MAPI; es un límite impuesto por algunos proveedores de almacén de mensajes. Para asegurar la interoperabilidad con los proveedores que se imponen, limitar sujetos a 128 bytes. 
  
Tenga en cuenta que algunos proveedores de almacén de mensajes no permitir **PR_SUBJECT** se escriban en un objeto stream con la interfaz [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) . 
  
No establezca **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Esta propiedad se establezca sólo en las respuestas y los mensajes reenviada. 
  

