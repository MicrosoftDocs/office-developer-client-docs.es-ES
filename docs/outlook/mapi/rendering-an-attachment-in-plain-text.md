---
title: Representación de datos adjuntos en texto sin formato
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 587736e7ca2f30468b169a33cea34927f857382c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410878"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Representación de datos adjuntos en texto sin formato

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para representar datos adjuntos en un mensaje con texto sin formato, recupere la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de los datos adjuntos y aplíquelo a los datos de la propiedad **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)). Hay dos maneras de recuperar **PR_RENDERING_POSITION**:
  
- Abra los datos adjuntos llamando al método **IMessage::OpenAttach** del mensaje **y, a continuación,** solicite la propiedad PR_RENDERING_POSITION llamando al método **IMAPIProp::GetProps** de los datos adjuntos. Para obtener más información, vea [IMessage::OpenAttach](imessage-openattach.md) e [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Llame al método **IMessage::GetAttachmentTable** del mensaje para obtener acceso a su tabla de datos adjuntos y recuperar la columna que contiene la **PR_RENDERING_POSITION** propiedad. De esta forma siempre es preferible. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
Tenga en cuenta que muchos almacenes de  mensajes compatible con RTF no calculan PR_RENDERING_POSITION hasta que un cliente solicite la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) de un mensaje. Hasta ese momento, **PR_RENDERING_POSITION** suele representar un valor aproximado. Los proveedores de almacén de mensajes pueden proporcionar a los clientes un valor aproximado para mejorar el rendimiento. 
  
La representación de un archivo o datos adjuntos binarios se almacena en su **PR_ATTACH_RENDERING** archivo. Tiene la opción de  recuperar PR_ATTACH_RENDERING de las mismas maneras que recuperó **PR_RENDERING_POSITION**: directamente desde los datos adjuntos o desde la tabla de datos adjuntos. Por **PR_ATTACH_RENDERING,** la primera estrategia, aunque requiere más tiempo, es más segura. Dado que algunos proveedores de almacén de mensajes truncan sus columnas de tabla a 255 bytes o, en algunos casos, 510 bytes, es difícil asegurarse de que la columna **PR_ATTACH_RENDERING** contiene la representación completa. Al recuperar la propiedad directamente desde los datos adjuntos, siempre estará completa. 
  
Ni OLE ni los datos adjuntos de **mensajes PR_ATTACH_RENDERING**. En su lugar, la representación de información para datos adjuntos ole 1 se almacena en la secuencia de texto del mensaje. Para los datos adjuntos ole 2, se almacena en una secuencia secundaria especial del objeto de almacenamiento. La representación de información para datos adjuntos de mensajes está disponible a través del administrador de formularios. 
  
 **Para recuperar la representación de datos adjuntos de un mensaje**
  
1. Use la clase de mensaje del mensaje para obtener acceso al administrador de formularios.
    
2. Obtenga acceso a la propiedad PR_MINI_ICON del administrador **de** formularios. Para obtener más información, **vea PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

