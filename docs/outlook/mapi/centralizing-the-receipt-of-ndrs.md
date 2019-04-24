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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332665"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Centralizar la recepción de NDR

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
**Para que los informes de no entrega (NDR) lleguen a una ubicación central cuando se ejecuten simultáneamente varias instancias del cliente**
  
1. Establecer **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) y **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) en los valores apropiados para la cuenta que va a recibir los informes. Cree el identificador de entrada llamando a [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) si es necesario. 
    
2. Comprenda que hay sistemas de mensajería que ignorarán la cuenta que ha solicitado para los informes y que los enviarán al autor. Reduzca el impacto que esto tendrá en los administradores que tendrán que mover los informes de la siguiente manera:
    
- Dar a su mensaje original una clase de mensaje distinta, como IPM. Note. MSNNews. Busque los mensajes entrantes con la clase rePort. IPM. Note. MSNNews. NDR y reenvíelos a la cuenta a la que ha pensado para llegar los informes. Al mismo tiempo, envíe un correo electrónico al sistema de mensajería que haya ignorado su cuenta de informe de no entrega para comunicar que debe seguir la propiedad **PR_REPORT_ENTRYID** . 
    
- La mayoría de los sistemas de mensajería que no respetan **PR_REPORT_ENTRYID** no cumplirán las convenciones de clase de mensaje de MAPI tampoco. Por lo tanto, recibirá algo parecido a una nota. Esto es un poco más difícil de tratar porque la entrada es tan variable. Mire el asunto y reenvíelo si encuentra algo de una lista de palabras que significa "no se puede entregar" o algo del asunto original. Prepárese para ajustar estas listas con el paso del tiempo. 
    

