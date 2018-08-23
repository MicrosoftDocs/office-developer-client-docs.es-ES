---
title: Centralizar la recepción de NDR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 16a150105211231af54ccfdc5d1565aeecea729e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579441"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Centralizar la recepción de NDR

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
**Para que los informes de no entrega (NDR) entran en una ubicación central cuando se ejecutan simultáneamente varias instancias del cliente**
  
1. Establezca **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) y **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) en los valores apropiados para la cuenta que va a recibir los informes. Crear el identificador de entrada mediante una llamada a [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) si es necesario. 
    
2. Saber que existen sistemas de mensajería que se va a omitir la cuenta que ha solicitado para los informes y enviarlos al autor de la. Reducir el impacto que esto tendrá en los administradores que necesitan para mover informes de alrededor de:
    
- Mayor que el mensaje original para una clase de mensaje distintos, como IPM. Note.MSNNews. Busque los mensajes entrantes con la clase Report.IPM.Note.MSNNews.NDR y reenviarlas a la cuenta pensado para llegar a los informes. Al mismo tiempo, enviar correo electrónico al sistema de mensajería que no tiene en cuenta su cuenta de informe de no entrega para comunicar que debe respetar la propiedad **PR_REPORT_ENTRYID** . 
    
- Sistemas de mensajería más que no se respetan **PR_REPORT_ENTRYID** no respeta las convenciones de clase de mensaje MAPI ya sea. Por lo tanto, recibirá algo parecido a una nota. Esto es un poco más difícil abordar los problemas con debido a que la entrada es por lo que la variable. Examine el asunto y reenviarlo si encuentra puede ser algo de una lista de palabras que Media "sin entregar" o algo desde el asunto de la original. Esté preparado para ajustar estas listas a través del tiempo. 
    

