---
title: Recepción de mensajes mediante el procesamiento de datos adjuntos personalizados de TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 046b537d41b318fa857ef77f1906edcf2c3aa2bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429323"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Recepción de mensajes mediante el procesamiento de datos adjuntos personalizados de TNEF

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para recibir un mensaje TNEF con procesamiento de datos adjuntos personalizado:
  
1. Importe todas las propiedades transmitibles (aquellas que admite el sistema de mensajería) del mensaje entrante a un nuevo mensaje MAPI. Esto incluye el texto del mensaje, que contiene el flujo de datos TNEF.
    
2. Identifique y decodifique los datos adjuntos especiales que contienen la secuencia TNEF.
    
3. Extraiga todos los datos adjuntos del mensaje entrante en datos adjuntos MAPI en el nuevo mensaje MAPI. Los nombres de archivo recuperados u otros marcadores de identificación de los datos adjuntos deben colocarse en la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) de los nuevos datos adjuntos para que el método [ITnef::ExtractProps](itnef-extractprops.md) pueda asociar posteriormente los datos adjuntos correctos con las etiquetas de datos adjuntos codificadas en el texto del mensaje. 
    
4. Cree una interfaz OLE **IStream** para ajustar la secuencia TNEF descodificada y usar ese objeto junto con el nuevo mensaje MAPI en una llamada a la función [OpenTnefStreamEx.](opentnefstreamex.md) 
    
5. Llame al **método ITnef::ExtractProps** para recuperar las propiedades no transmitibles del mensaje desde el flujo de datos de TNEF. 
    
6. Llame al [método ITnef::OpenTaggedBody](itnef-opentaggedbody.md) con las marcas MAPI_CREATE y MAPI_MODIFY establecidas. Esta llamada quita las etiquetas de datos adjuntos del texto del mensaje y las convierte en información de posición de datos adjuntos en el mensaje MAPI. 
    
7. Entregue el mensaje a través de la cola MAPI.
    

