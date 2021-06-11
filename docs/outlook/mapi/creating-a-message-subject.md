---
title: Creación de un asunto de mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332966"
---
# <a name="creating-a-message-subject"></a>Creación de un asunto de mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El asunto de un mensaje, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), es una propiedad opcional, que se usa para resumir la intención de un mensaje. Si decides establecerlo, haz que sea una cadena de caracteres de 128 bytes o menos. El límite de 128 bytes no es un límite impuesto por MAPI; es un límite impuesto por algunos proveedores de almacenes de mensajes. Para garantizar la interoperabilidad con los proveedores que sí lo imponen, limite los sujetos a 128 bytes. 
  
Tenga en cuenta que algunos proveedores de almacén de mensajes **PR_SUBJECT** que se escriban en una secuencia con la [interfaz IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
  
No establezca **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); esta propiedad solo se establece en las respuestas y los mensajes reenviados. 
  

