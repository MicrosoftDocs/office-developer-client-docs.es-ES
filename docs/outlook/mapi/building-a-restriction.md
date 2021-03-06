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
  
Para crear una restricción, una aplicación cliente crea una jerarquía de una o varias estructuras de restricción de varios tipos y pasa un puntero a la jerarquía al método [IMAPITable::Restrict](imapitable-restrict.md) o [IMAPITable::FindRow.](imapitable-findrow.md) La ilustración que se muestra a continuación y el ejemplo de código del [código](sample-restriction-code.md) de restricción de ejemplo muestran cómo se implementa una restricción típica con estructuras de restricción vinculadas de diferentes tipos. 

En este ejemplo, un usuario de una aplicación cliente está intentando encontrar todos los mensajes que contienen la palabra "volea" en la línea de asunto y se enviaron a Sue desde Sam. En primer lugar, se asigna una [estructura SRestriction](srestriction.md) genérica. Esta estructura se convierte en la base de otras llamadas a la función [MAPIAllocateMore](mapiallocatemore.md) para crear estructuras [vinculadas de SRestriction](srestriction.md) y [SPropValue](spropvalue.md) que se pueden liberar con una sola llamada a [MAPIFreeBuffer](mapifreebuffer.md). Dado que los criterios que se deben aplicar al conjunto de mensajes están en tres partes, la estructura de restricción de nivel superior es una **restricción AND.** El miembro **cRes** de la estructura [SAndRestriction](sandrestriction.md) se establece en 3 para indicar las tres restricciones que se deben evaluar y su miembro **lpRes** se establece en una matriz de tres miembros de estructuras **SRestriction.** 
  
Para buscar mensajes que se envían a un destinatario determinado, es necesario buscar en la tabla de destinatarios cada mensaje en lugar del mensaje en sí. Se usa una restricción de subobjeto para realizar la búsqueda de tabla de destinatarios. Por lo tanto, el primer miembro de la matriz apunta a una estructura [SSubRestriction](ssubrestriction.md) con su **miembro ulSubObject** establecido en **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). A continuación, para especificar qué buscar en la tabla de destinatarios, se usa una restricción de contenido. 
  
El segundo y tercer miembros de la matriz son más sencillos. Ambos apuntan a estructuras de restricción de contenido, una para buscar mensajes que tienen una propiedad **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) establecida en "Sam" y otra que tiene una propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) establecida en "volea".
  
**Implementación de restricción**
  
![Implementación de restricción](media/amapi_61.gif "Implementación de restricción")
  
## <a name="see-also"></a>Vea también

- [Tablas MAPI](mapi-tables.md)

