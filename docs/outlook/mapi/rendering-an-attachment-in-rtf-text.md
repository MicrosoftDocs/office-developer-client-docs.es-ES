---
title: Representar datos adjuntos en texto RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5d8fc10f876408d616c5acefb664ba5d61c927a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562977"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Representar datos adjuntos en texto RTF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Formato de texto de Rich (RTF)-tener en cuenta los clientes pueden recuperar información de posición de representación de texto del mensaje RTF mediante busca la siguiente secuencia de escape en la propiedad del mensaje **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)):
  
 `\objattph`
  
 **Para buscar información de representación en texto con formato**
  
1. Llame a **IMessage::GetAttachmentTable** para obtener acceso a la tabla de datos adjuntos del mensaje. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Crear una restricción de propiedad que limita la tabla a las filas que tienen **PR_RENDERING_POSITION** no es igual a -1. Para obtener más información, vea **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
    
3. Llamar a **IMAPITable:: Restrict** para aplicar la restricción. Para obtener más información, vea [IMAPITable:: Restrict](imapitable-restrict.md).
    
4. Llamar a **SortTable** para ordenar los datos adjuntos. Para obtener más información, vea [SortTable](imapitable-sorttable.md).
    
5. Llamar a **IMAPITable:: QueryRows** para recuperar las filas correspondientes. Para obtener más información, vea [IMAPITable:: QueryRows](imapitable-queryrows.md).
    
6. Llamar al método **IMAPIProp::OpenProperty** del mensaje para recuperar **PR_RTF_COMPRESSED** con la interfaz **IStream** . Para obtener más información, vea [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y **PR_RTF_COMPRESSED**.
    
7. Examinar la secuencia, busca el marcador de posición de representación, `\objattph`. El carácter que sigue a este marcador de posición es el lugar para los datos adjuntos siguiente de la tabla ordenada.
    

