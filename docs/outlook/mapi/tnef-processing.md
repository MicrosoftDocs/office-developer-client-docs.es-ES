---
title: Procesamiento TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: 066ad3dfb64161e326b92fef7774d5b3b9461d8a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339602"
---
# <a name="tnef-processing"></a>Procesamiento TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La siguiente serie de acciones describe cómo los transportes usan métodos TNEF para procesar mensajes salientes y entrantes.
  
 **Para enviar un mensaje que incluya una secuencia TNEF**
  
1. Procesar las propiedades del mensaje admitidas por el sistema de mensajería.
    
2. Marque el mensaje de una manera específica para que el proveedor de transporte receptor pueda determinar que el mensaje requiere procesamiento TNEF. Por ejemplo, un proveedor de transporte TNEF que envía a un sistema de mensajería SMTP puede agregar un campo de encabezado personalizado como "X-CONTAINS-TNEF" para indicar que el mensaje contiene datos TNEF.
    
3. Obtenga un objeto TNEF y úselo para encapsular las propiedades de mensaje no admitidas por el sistema de mensajería en una secuencia TNEF.
    
4. Codifica la secuencia TNEF mediante el modelo de datos adjuntos del sistema de mensajería. Por ejemplo, si el modelo de datos adjuntos subyacente es codificar datos adjuntos y anexarlos al texto del mensaje, el proveedor de transporte debe codificar la secuencia TNEF en otro archivo adjunto. El proveedor de transporte también debe implementar un método para reconocer qué datos adjuntos contienen la secuencia TNEF codificada cuando recibe un mensaje. La forma estándar de marcar estos datos adjuntos es darle un nombre de archivo de datos adjuntos de "WINMAIL. DAT". Si el proveedor de transporte hace esto, cualquier otro proveedor de transporte habilitado para TNEF que siga esta convención podrá interoperar con ella.
    
5. Utilice los métodos de la interfaz [ITnef : IUnknown](itnefiunknown.md) para insertar etiquetas que describan las posiciones de los datos adjuntos del mensaje en el texto del mensaje. 
    
6. Accede al texto del mensaje etiquetado a través [de los métodos IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) y envíalo al sistema de mensajería. 
    
 **Para recuperar propiedades encapsuladas**
  
1. Escriba las propiedades admitidas por el sistema de mensajería en un nuevo mensaje, incluido el texto del mensaje etiquetado que contiene las propiedades encapsuladas.
    
2. Descodificar la secuencia TNEF de los datos adjuntos adecuados.
    
3. Descodificar cualquier otro archivo adjunto y escribirlos en nuevos datos adjuntos MAPI en un mensaje.
    
4. Abra la secuencia TNEF para la decodificación mediante la [función OpenTnefStreamEx.](opentnefstreamex.md) 
    
5. Utilice el [método ITnef::ExtractProps](itnef-extractprops.md) para descodificar la secuencia TNEF y escribir las propiedades encapsuladas en el nuevo mensaje. Las propiedades codificadas que sean duplicados de propiedades no codificadas sobrescribirán las propiedades no codificadas cuando se descodifican las propiedades codificadas. 
    
6. Utilice el [método ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para analizar el texto del mensaje y recuperar las posiciones de datos adjuntos de las etiquetas del texto del mensaje. 
    

