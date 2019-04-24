---
title: Procesamiento de TNEF
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
# <a name="tnef-processing"></a>Procesamiento de TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La siguiente serie de acciones describe cómo los transportes usan métodos TNEF para procesar los mensajes entrantes y salientes.
  
 **Para enviar un mensaje que incluya una secuencia TNEF**
  
1. Procesa las propiedades del mensaje que son compatibles con el sistema de mensajería.
    
2. Marque el mensaje de una manera específica de implementación para que el proveedor de transporte receptor pueda determinar que el mensaje requiere procesamiento TNEF. Por ejemplo, un proveedor de transporte TNEF que envíe a un sistema de mensajería SMTP puede Agregar un campo de encabezado personalizado como "X-conTAINs-TNEF" para indicar que el mensaje contiene datos TNEF.
    
3. Obtener un objeto TNEF y usarlo para encapsular las propiedades del mensaje no admitido por el sistema de mensajería en una secuencia TNEF.
    
4. Codifique la secuencia TNEF mediante el modelo de datos adjuntos del sistema de mensajería. Por ejemplo, si el modelo de datos adjuntos subyacente es uuencode y los anexa al texto del mensaje, el proveedor de transporte deberá CODIFICAr la secuencia TNEF en otro archivo de datos adjuntos. El proveedor de transporte también debe implementar un método para reconocer qué datos adjuntos contienen el flujo TNEF codificado cuando recibe un mensaje. La forma estándar de marcar estos datos adjuntos es proporcionarle un nombre de archivo de datos adjuntos de "WINMAIL. DAT ". Si el proveedor de transporte realiza esta operación, cualquier otro proveedor de transporte habilitado para TNEF que siga esta Convención podrá interoperar con ella.
    
5. Use [ITnef:](itnefiunknown.md) métodos de interfaz IUnknown para insertar etiquetas que describen las posiciones de los datos adjuntos de los mensajes en el texto del mensaje. 
    
6. Obtener acceso al texto del mensaje etiquetado mediante métodos [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) y enviarlo al sistema de mensajería. 
    
 **Para recuperar propiedades encapsuladas**
  
1. Escriba las propiedades admitidas por el sistema de mensajería en un mensaje nuevo, incluido el texto del mensaje etiquetado que contiene las propiedades encapsuladas.
    
2. Descodifique el flujo TNEF de los datos adjuntos correctos.
    
3. Descodifique los demás datos adjuntos y escríbalos en nuevos datos adjuntos MAPI en un mensaje.
    
4. Abra la secuencia TNEF para descodificar mediante la función [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Utilice el método [ITnef:: ExtractProps](itnef-extractprops.md) para descodificar la secuencia TNEF y escribir las propiedades encapsuladas en el nuevo mensaje. Las propiedades codificadas que son duplicados de propiedades no codificadas sobrescribirán las propiedades no codificadas cuando se descodifiquen las propiedades codificadas. 
    
6. Use el método [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) para analizar el texto del mensaje para recuperar las posiciones de datos adjuntos de las etiquetas en el texto del mensaje. 
    

