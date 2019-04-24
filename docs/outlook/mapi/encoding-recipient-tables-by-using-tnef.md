---
title: Codificar tablas de destinatarios mediante TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339406"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Codificar tablas de destinatarios mediante TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La codificación de una tabla de destinatarios en la secuencia TNEF rara vez es necesaria, ya que la mayoría de los sistemas de mensajería admiten listas de destinatarios directamente. En general, las propiedades del destinatario se transmiten en el encabezado del mensaje. Cuando se necesita la inclusión de la tabla de destinatarios, TNEF puede codificar la tabla de destinatarios como parte de su procesamiento habitual. Esto se realiza durante la fase inicial del procesamiento TNEF. El proveedor de transporte puede incluir la tabla de destinatarios del mensaje llamando al método [ITnef:: AddProps](itnef-addprops.md) con la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) especificada en la lista de inclusión. TNEF obtiene la tabla de destinatarios del mensaje, consulta el conjunto de columnas y procesa todas las filas de la tabla en la secuencia TNEF.
  
Hay disponible un método alternativo si el proveedor de transporte necesita modificar la tabla de destinatarios antes de codificarla. El proveedor de transporte puede construir la tabla necesaria y, a continuación, llamar al método [ITnef:: EncodeRecips](itnef-encoderecips.md) . Si se pasa NULL en el parámetro _lpRecipTable_ , la tabla de destinatarios se obtiene directamente del mensaje, tal y como se describe para **ITnef:: AddProps**.
  

