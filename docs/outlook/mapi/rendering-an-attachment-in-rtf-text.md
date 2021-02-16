---
title: Representación de datos adjuntos en texto RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439796"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Representación de datos adjuntos en texto RTF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes con formato de texto enriquecido (RTF) pueden recuperar información de posición de representación del texto del mensaje RTF buscando la siguiente secuencia de escape en la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) del mensaje:
  
 `\objattph`
  
 **Para localizar la información de representación en texto con formato**
  
1. Llame **a IMessage::GetAttachmentTable** para obtener acceso a la tabla de datos adjuntos del mensaje. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Cree una restricción de propiedad que limite la tabla a las filas PR_RENDERING_POSITION **que** no son iguales a -1. Para obtener más información, **vea PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
    
3. Llame **a IMAPITable::Restrict** para aplicar la restricción. Para obtener más información, [vea IMAPITable::Restrict](imapitable-restrict.md).
    
4. Llame **a IMAPITable::SortTable** para ordenar los datos adjuntos. Para obtener más información, [vea IMAPITable::SortTable](imapitable-sorttable.md).
    
5. Llame **a IMAPITable::QueryRows** para recuperar las filas apropiadas. Para obtener más información, [vea IMAPITable::QueryRows](imapitable-queryrows.md).
    
6. Llame al método **IMAPIProp::OpenProperty** del mensaje para recuperar **PR_RTF_COMPRESSED** con la **interfaz IStream.** Para obtener más información, [vea IMAPIProp::OpenProperty](imapiprop-openproperty.md) y **PR_RTF_COMPRESSED**.
    
7. Examinar la secuencia, buscando el marcador de posición de representación,  `\objattph` . El carácter que sigue a este marcador de posición es el lugar para los siguientes datos adjuntos en la tabla ordenada.
    

