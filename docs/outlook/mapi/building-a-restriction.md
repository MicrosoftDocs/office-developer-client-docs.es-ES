---
title: Crear una restricción
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 38182abd922cd5806a14b6541c22ce675b997387
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422513"
---
# <a name="building-a-restriction"></a>Crear una restricción

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para crear una restricción, una aplicación cliente crea una jerarquía de una o varias estructuras de restricción de distintos tipos y pasa un puntero a la jerarquía al método [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md) . La ilustración siguiente y el código de ejemplo de [ejemplo de código de restricción de ejemplo](sample-restriction-code.md) demuestran cómo se implementa una restricción típica con estructuras de restricción vinculadas de distintos tipos. 

En este ejemplo, un usuario de una aplicación cliente está intentando encontrar todos los mensajes que contienen la palabra "Volleyball" en la línea de asunto y se enviaron a Sue desde Sam. En primer lugar, se asigna una estructura [SRestriction](srestriction.md) genérica. Esta estructura se convierte en la base para otras llamadas a la función [MAPIAllocateMore](mapiallocatemore.md) para crear estructuras de [SRestriction](srestriction.md) y [SPropValue](spropvalue.md) vinculadas que se pueden liberar con una sola llamada a [MAPIFreeBuffer](mapifreebuffer.md). Debido a que los criterios que se deben aplicar al conjunto de mensajes se encuentra en tres partes, la estructura de restricción de nivel superior es una restricción **and** . El miembro **cRes** de la estructura [SAndRestriction](sandrestriction.md) se establece en 3 para indicar las tres restricciones que se van a evaluar y su miembro **lpRes** se establece en una matriz de tres miembros de **SRestriction** estructuras. 
  
Para buscar los mensajes que se envían a un destinatario en particular, es necesario buscar en la tabla de destinatarios cada mensaje en lugar de hacerlo en el propio mensaje. Se usa una restricción de subobjeto para realizar la búsqueda de la tabla de destinatarios. Por lo tanto, el primer miembro de la matriz apunta a una estructura [SSubRestriction](ssubrestriction.md) con su miembro **UlSubObject** establecido en **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). A continuación, para especificar qué desea buscar en la tabla de destinatarios, se usa una restricción de contenido. 
  
El segundo y el tercer miembro de la matriz son más sencillos. Ambos apuntan a estructuras de restricción de contenido, una para buscar mensajes que tienen una propiedad **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) establecida en "Sam" y otra que tiene una propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) establecida en " Volleyball ".
  
**Implementación de restricción**
  
![Implementación de restricción] (media/amapi_61.gif "Implementación de restricción")
  
## <a name="see-also"></a>Ver también

- [Tablas MAPI](mapi-tables.md)

