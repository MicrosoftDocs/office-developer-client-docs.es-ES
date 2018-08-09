---
title: Creación de una restricción
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3b40c8433f93237db2ae4fd5449fe8a0da486539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816499"
---
# <a name="building-a-restriction"></a>Creación de una restricción

**Hace referencia a**: Outlook 
  
Para crear una restricción, una aplicación de cliente crea una jerarquía de uno o más estructuras de restricción de varios tipos y pasa un puntero a la jerarquía al método [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md) . La ilustración siguiente y el ejemplo de código en [Código de restricción de ejemplo](sample-restriction-code.md) demuestran cómo se implementa una restricción típica con estructuras de restricción vinculado de distintos tipos. 

En este ejemplo, un usuario de una aplicación cliente intenta encontrar todos los mensajes que contienen la palabra "voleibol" en la línea de asunto y se enviaban a Sue desde Sam. En primer lugar, se asigna una estructura [SRestriction](srestriction.md) genérica. Esta estructura se convierte en la base para otras llamadas a la función [MAPIAllocateMore](mapiallocatemore.md) crear estructuras de [SRestriction](srestriction.md) y [SPropValue](spropvalue.md) vinculadas que se pueden liberar con una sola llamada a [MAPIFreeBuffer](mapifreebuffer.md). Debido a que los criterios que se debe aplicar al conjunto de mensajes se encuentra en tres partes, la estructura de restricción del nivel superior es una restricción de **y** . Miembro de **cRes** de la estructura [SAndRestriction](sandrestriction.md) se establece en 3 para indicar las tres restricciones para evaluar y su miembro **lpRes** se establece en una matriz de tres miembros de estructuras **SRestriction** . 
  
Para buscar los mensajes que se envían a un destinatario concreto, es necesario buscar en la tabla de destinatarios para cada mensaje en lugar del propio mensaje. Una restricción de subobjetos se utiliza para realizar la búsqueda de la tabla de destinatarios. Por lo tanto, el primer miembro de los puntos de la matriz en una estructura de [SSubRestriction](ssubrestriction.md) con su **ulSubObject** conjunto de miembros a **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). A continuación, para especificar qué se va a buscar en la tabla de destinatarios, se utiliza una restricción de contenido. 
  
La segundo y terceros los miembros de la matriz son más sencillos. Ambas apuntan a estructuras de restricción de contenido, uno para buscar los mensajes que tienen una propiedad **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) establecida en "Sam" y otro que tiene una propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) que se establece en" voleibol."
  
**Implementación de restricción**
  
![Implementación de restricción] (media/amapi_61.gif "Implementación de restricción")
  
## <a name="see-also"></a>Vea también

- [Tablas MAPI](mapi-tables.md)

