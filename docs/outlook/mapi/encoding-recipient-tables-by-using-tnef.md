---
title: Codificación de tablas de destinatarios mediante TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417962"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Codificación de tablas de destinatarios mediante TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La codificación de una tabla de destinatarios en la secuencia TNEF rara vez es necesaria, ya que la mayoría de los sistemas de mensajería admiten listas de destinatarios directamente. En general, las propiedades del destinatario se transmiten en el encabezado del mensaje. Cuando es necesaria la inclusión de la tabla de destinatarios, TNEF puede codificar la tabla de destinatarios como parte de su procesamiento habitual. Esto se realiza durante la fase inicial del procesamiento de TNEF. El proveedor de transporte puede incluir la tabla de destinatarios del mensaje llamando al método [ITnef::AddProps](itnef-addprops.md) con la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) especificada en la lista de inclusión. TNEF obtiene la tabla de destinatarios del mensaje, consulta el conjunto de columnas y procesa todas las filas de la tabla en la secuencia TNEF.
  
Hay un método alternativo disponible si el proveedor de transporte necesita modificar la tabla de destinatarios antes de codificarse. El proveedor de transporte puede construir la tabla necesaria y, a continuación, llamar al [método ITnef::EncodeRecips.](itnef-encoderecips.md) Si se pasa NULL en el parámetro  _lpRecipTable,_ la tabla de destinatarios se toma directamente del mensaje tal como se describe para **ITnef::AddProps**.
  

