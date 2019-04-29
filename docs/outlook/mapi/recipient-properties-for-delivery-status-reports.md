---
title: Propiedades de destinatario para informes de estado de entrega
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9b2e287e-1cf8-4b8f-b92c-a065ed264d02
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 784cac21aac5de18952f3768af9b8f189f604981
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411088"
---
# <a name="recipient-properties-for-delivery-status-reports"></a>Propiedades de destinatario para informes de estado de entrega

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las siguientes propiedades están presentes para los informes de estado de entrega de los destinatarios. **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) no se usa en informes de no entrega. **PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md)) y **PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)) solo se usan en informes de no entrega.
  
**Título de la tabla**

|**Property**|**Decription**|
|:-----|:-----|
|**PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md))  <br/> |Contiene la fecha y la hora en que se entregó el mensaje original.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Contiene el nombre para mostrar de un objeto MAPI determinado.  <br/> |
|**** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Contiene un identificador de entrada MAPI que se usa para abrir y editar las propiedades de un objeto MAPI en particular.  <br/> |
|**PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md))  <br/> |Contiene un código de diagnóstico que forma parte de un informe de no entrega.  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Contiene una cadena de texto que identifica la clase de mensaje definida por el remitente, como IPM. Note.  <br/> |
|**PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md))  <br/> |Contiene un motivo codificado para la no entrega que forma parte de un informe de no entrega.  <br/> |
|**PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))  <br/> |Contiene el nombre para mostrar original de una entrada copiada de una libreta de direcciones en una libreta personal de direcciones o en otra libreta de direcciones de escritura.  <br/> |
|**PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))  <br/> |Contiene el identificador de entrada original para una entrada copiada de una libreta de direcciones en una libreta personal de direcciones u otra libreta de direcciones grabable.  <br/> |
|**PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md))  <br/> |Contiene la clave de búsqueda original de una entrada copiada de una libreta de direcciones en una libreta personal de direcciones u otra libreta de direcciones grabable.  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Contiene el tipo de destinatario de un destinatario del mensaje.  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |Contiene texto opcional para un informe generado por el sistema de mensajería.  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |Contiene la fecha y la hora en que el sistema de mensajería generó un informe.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Contiene una clave comparable binaria que identifica los objetos correlacionados para una búsqueda.  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Contiene un valor que se usa para asociar un icono a una fila concreta de una tabla.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Contiene el tipo de un objeto.  <br/> |
   

