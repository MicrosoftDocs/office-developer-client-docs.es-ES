---
title: Representar datos adjuntos en texto sin formato
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 38db1d18f240188c7566a57afa23291a307446dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820512"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Representar datos adjuntos en texto sin formato

  
  
**Hace referencia a**: Outlook 
  
Para representar un dato adjunto en un mensaje con texto sin formato, recuperar la propiedad de **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de los datos adjuntos y se aplican a los datos de la **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) propiedad. Hay dos formas de recuperar **PR_RENDERING_POSITION**:
  
- Abra los datos adjuntos mediante una llamada al método **IMessage::OpenAttach** del mensaje y, a continuación, pida la propiedad **PR_RENDERING_POSITION** mediante una llamada al método de **IMAPIProp::GetProps** de los datos adjuntos. Para obtener más información, vea [IMessage::OpenAttach](imessage-openattach.md) y [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Llamar al método **IMessage::GetAttachmentTable** del mensaje para tener acceso a su tabla de datos adjuntos y recuperar la columna que contiene la propiedad **PR_RENDERING_POSITION** . De este modo, siempre es preferible. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
Tenga en cuenta que muchos almacenes de mensaje compatibles con RTF no calculan **PR_RENDERING_POSITION** hasta que un cliente solicita la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) de un mensaje. Hasta ese momento, **PR_RENDERING_POSITION** normalmente representa un valor aproximado. Los proveedores de almacén de mensajes se permiten proporcionar a los clientes con un valor aproximado para mejorar el rendimiento. 
  
La representación de un archivo o datos adjuntos binarios se almacena en su propiedad **PR_ATTACH_RENDERING** . Tiene la opción de recuperación de **PR_ATTACH_RENDERING** de la misma manera como recuperar **PR_RENDERING_POSITION**: directamente desde los datos adjuntos o desde la tabla de datos adjuntos. Para **PR_ATTACH_RENDERING**, la primera estrategia, aunque más tiempo, es más seguro. Dado que algunos proveedores de almacenes de mensaje truncan sus columnas de tabla a 255 bytes o, en algunos casos bytes 510, es difícil para asegurarse de que la columna **PR_ATTACH_RENDERING** contiene la representación completa. Al recuperar la propiedad directamente de los datos adjuntos, siempre será completa. 
  
Los datos adjuntos OLE ni mensaje establecer **PR_ATTACH_RENDERING**. En su lugar, se almacena información de representación de los datos adjuntos OLE 1 en la secuencia de texto del mensaje. Los datos adjuntos OLE 2, se almacena en una secuencia de secundarios especiales del objeto de almacenamiento. Información para los datos adjuntos de mensajes de representación está disponible a través del Administrador de formulario. 
  
 **Para recuperar la representación de datos adjuntos del mensaje**
  
1. Use la clase de mensaje del mensaje para tener acceso al administrador de formulario.
    
2. Obtener acceso a la propiedad **PR_MINI_ICON** del director de formulario. Para obtener más información, vea **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

