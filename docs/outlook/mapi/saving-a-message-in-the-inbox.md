---
title: Guardar un mensaje en la bandeja de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357536"
---
# <a name="saving-a-message-in-the-inbox"></a>Guardar un mensaje en la bandeja de entrada

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para almacenar un mensaje en la bandeja de entrada sin destinatarios**
  
1. Llame a [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar el identificador de entrada de la bandeja de entrada. 
    
2. Llame a [IMsgStore:: OpenEntry](imsgstore-openentry.md) para abrir la bandeja de entrada y recuperar un puntero. 
    
3. Llame al método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) de la bandeja de entrada para crear el mensaje. 
    
4. Llame al método [IMAPIProp:: SetProps](imapiprop-setprops.md) del mensaje para agregar el **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) y **PR_SUBJECT** ([ PidTagSubject](pidtagsubject-canonical-property.md)) propiedades. 
    
5. Cree todos los datos adjuntos, establezca sus propiedades y guárdelo. Para obtener información detallada acerca de la adición de datos adjuntos a mensajes, vea [creación de datos adjuntos de un mensaje](creating-a-message-attachment.md).
    
6. Llame a **IMessage:: SaveChanges** para guardar el mensaje. En este momento, aparecerá en la tabla de contenido de la bandeja de entrada. 
    
Si desea guardar un mensaje intermittantly antes de que aparezca en la tabla de contenido de la bandeja de entrada, créelo en una carpeta oculta, como la carpeta raíz del subárbol IPM y, a continuación, muévalo a la bandeja de entrada. 
  

