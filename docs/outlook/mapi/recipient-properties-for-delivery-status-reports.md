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
ms.openlocfilehash: 58711a18fa6dc512cca10644437bee2ecd4d2143
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593000"
---
# <a name="recipient-properties-for-delivery-status-reports"></a>Propiedades de destinatario para informes de estado de entrega

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las siguientes propiedades están presentes para informes de estado de entrega para los destinatarios. **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) no se usa en los informes de no entrega. **PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md)) y **PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)) sólo se utilizan en informes de no entrega.
  
**Título de la tabla**

|**Propiedad**|**Descripción**|
|:-----|:-----|
|**PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md))  <br/> |Contiene la fecha y la hora a la que se ha entregado el mensaje original.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Contiene el nombre para mostrar para un determinado objeto MAPI.  <br/> |
|**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Contiene un identificador de entrada MAPI utilizado para abrir y editar las propiedades de un determinado objeto MAPI.  <br/> |
|**PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md))  <br/> |Contiene un código de diagnóstico que forma parte de un informe de no entrega.  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Contiene una cadena de texto que identifica la clase de mensaje definido por el remitente, como IPM. Tenga en cuenta.  <br/> |
|**PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md))  <br/> |Contiene un motivo codificado de no entrega que forma parte de un informe de no entrega.  <br/> |
|**PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))  <br/> |Contiene el nombre para mostrar original para una entrada de copia de una libreta de direcciones a otra libreta de direcciones puede escribir o de una libreta de direcciones personales.  <br/> |
|**PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))  <br/> |Contiene el identificador de entrada original para una entrada de copiado de otra libreta de direcciones grabable o de una libreta de direcciones a una libreta de direcciones personales.  <br/> |
|**PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md))  <br/> |Contiene la clave de búsqueda original de una entrada copiada de otra libreta de direcciones grabable o de una libreta de direcciones a una libreta de direcciones personales.  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Contiene el tipo de destinatario para un destinatario del mensaje.  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |Contiene texto opcional de un informe generado por el sistema de mensajería.  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |Contiene la fecha y la hora cuando el sistema de mensajería genera un informe.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Contiene una clave binario comparable que identifica objetos correlacionados para una búsqueda.  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Contiene un valor que se utiliza para asociar un icono a una fila de una tabla determinada.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Contiene el tipo de un objeto.  <br/> |
   

