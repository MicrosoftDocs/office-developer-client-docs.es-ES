---
title: Codificar tablas de destinatario con TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: aa2120b5d64eece76f8882489de4388b04afa053
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591348"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Codificar tablas de destinatario con TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La codificación de una tabla de destinatario en la secuencia TNEF es rara vez es necesaria dado que los sistemas de mensajería más admiten las listas de destinatarios directamente. En general, las propiedades del destinatario se transmiten en el encabezado del mensaje. Cuando es necesaria la inclusión de la tabla de destinatarios, TNEF puede codificar la tabla de destinatarios como parte de su procesamiento habitual. Esto se realiza durante la fase inicial de procesamiento de TNEF. El proveedor de transporte puede incluir la tabla de destinatarios del mensaje llamando al método [ITnef::AddProps](itnef-addprops.md) con la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) especificada en la lista de inclusión. TNEF Obtiene la tabla de destinatarios del mensaje, consulta el conjunto de columnas y procesa cada fila de la tabla en la secuencia de TNEF.
  
Un método alternativo está disponible si el proveedor de transporte que se necesita modificar la tabla de destinatarios antes de que se codifica. El proveedor de transporte puede construir la tabla es necesaria y, a continuación, llame al método [ITnef::EncodeRecips](itnef-encoderecips.md) . Si se pasa NULL en el parámetro _lpRecipTable_ , tal como se describe para **ITnef::AddProps**, a continuación, la tabla de destinatarios se toma directamente desde el mensaje.
  

