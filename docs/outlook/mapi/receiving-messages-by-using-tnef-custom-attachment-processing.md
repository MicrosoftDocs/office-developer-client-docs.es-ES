---
title: Recibir mensajes a través del procesamiento de datos adjuntos personalizado TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: 'Última modificación: 07 de diciembre de 2015'
ms.openlocfilehash: 67c202e5130bd35e1277c5260bc1702043eadd95
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588030"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Recibir mensajes a través del procesamiento de datos adjuntos personalizado TNEF

 
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Para recibir un mensaje TNEF con procesamiento de datos adjuntos personalizado:
  
1. Importar todas las propiedades transmisible: aquellos que admite el sistema de mensajería, desde el mensaje entrante en un nuevo mensaje de MAPI. Esto incluye el texto del mensaje, que contiene la secuencia de datos TNEF.
    
2. Identificar y descodificar los datos adjuntos especial que contiene la secuencia TNEF.
    
3. Extraiga todos los datos adjuntos del mensaje entrante en datos adjuntos de MAPI en el nuevo mensaje MAPI. Los nombres de archivo recuperado, u otros marcadores de identificación en los datos adjuntos, deben colocarse en la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) de los nuevos datos adjuntos por lo que el método [ITnef::ExtractProps](itnef-extractprops.md) más adelante se puede asociar los datos adjuntos correcto con las etiquetas de datos adjuntos codificadas en el texto del mensaje. 
    
4. Crear una interfaz **IStream** OLE para ajuste alrededor de la secuencia TNEF descodificada y usar ese objeto junto con el nuevo mensaje MAPI en una llamada a la función [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Llame al método **ITnef::ExtractProps** para recuperar las propiedades de nontransmittable en el mensaje de la secuencia de datos TNEF. 
    
6. Llame al método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) con el conjunto de indicadores MAPI_CREATE y MAPI_MODIFY. Esta llamada quita las etiquetas de datos adjuntos desde el texto del mensaje y los convierte en información de posición de datos adjuntos en el mensaje MAPI. 
    
7. Entregar el mensaje a través de la cola de MAPI.
    

