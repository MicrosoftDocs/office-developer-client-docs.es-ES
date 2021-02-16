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
ms.openlocfilehash: af2531076755d1e183409f50fe1a0c97d28063f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405859"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Centralizar la recepción de NDR

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
**Para que los informes nondelivery (NDRs) lleguen a una ubicación central cuando varias instancias del cliente se ejecutan simultáneamente**
  
1. Establezca **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) y PR_REPORT_SEARCH_KEY ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) **en** los valores adecuados para la cuenta que va a recibir los informes. Cree el identificador de entrada llamando a [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) si es necesario. 
    
2. Comprenda que hay sistemas de mensajería que ignorarán la cuenta que ha solicitado para los informes y las enviarán al autor de la solicitud. Reduzca el impacto que esto tendrá en los administradores que tendrán que mover los informes:
    
- Dar al mensaje original una clase de mensaje distinta, como IPM. Note.MSNNews. Busque mensajes entrantes con la clase Report.IPM.Note.MSNNews.NDR y reenvía a la cuenta a la que desea que se presenten los informes. Al mismo tiempo, envíe un correo electrónico al sistema de mensajería que omitió su cuenta de informe de no entrega para comunicar que debe respetar la **propiedad PR_REPORT_ENTRYID** cliente. 
    
- La mayoría de los sistemas de mensajería **que PR_REPORT_ENTRYID** no respetarán las convenciones de clase de mensaje MAPI. Por lo tanto, recibirá algo parecido a una nota. Esto es un poco más difícil de tratar porque la entrada es tan variable. Mira el asunto y reenvía si encuentras algo de una lista de palabras que significan "no se puede entregar" o algo del tema original. Esté preparado para ajustar estas listas con el tiempo. 
    

