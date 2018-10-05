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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399573"
---
# <a name="tnef-processing"></a>Procesamiento de TNEF

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
La siguiente serie de acciones describe cómo usar los transportes los métodos TNEF para procesar los mensajes entrantes y salientes.
  
 **Para enviar un mensaje que incluye una secuencia TNEF**
  
1. Proceso de las propiedades del mensaje que son compatibles con el sistema de mensajería.
    
2. Marcar el mensaje en una implementación específica manera para que el proveedor de transporte receptora puede determinar que el mensaje requiere procesamiento de TNEF. Por ejemplo, un proveedor de transporte TNEF envío a un sistema de mensajería SMTP puede agregar un campo de encabezado personalizado como "X-contiene-TNEF" para indicar que el mensaje contiene datos TNEF.
    
3. Obtener un objeto TNEF y usarlo para encapsular las propiedades de mensaje no compatibles con el sistema de mensajería en una secuencia TNEF.
    
4. Codificar la secuencia TNEF mediante el modelo de datos adjuntos del sistema de mensajería. Por ejemplo, si el modelo de datos adjuntos subyacente consiste en datos adjuntos uuencode y agregarlos al texto del mensaje, el proveedor de transporte debe uuencode la secuencia TNEF en otro objeto attachment. El proveedor de transporte también debe implementar un método para reconocer qué datos adjuntos contienen la secuencia TNEF codificada cuando recibe un mensaje. La forma estándar para marcar estos datos adjuntos es asignarle un nombre de archivo de datos adjuntos de "WINMAIL. RÁPIDO". Si su proveedor de transporte para ello, otros proveedores de transporte TNEF habilitado que siguen esta convención podrán interoperar con él.
    
5. Uso [ITnef: IUnknown](itnefiunknown.md) métodos para insertar etiquetas que describe las posiciones de los datos adjuntos del mensaje en el texto del mensaje de interfaz. 
    
6. Obtener acceso el texto del mensaje con etiqueta a través de métodos de [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) y enviarlo al sistema de mensajería. 
    
 **Para recuperar propiedades encapsuladas**
  
1. Escribir las propiedades compatibles con el sistema de mensajería en un mensaje nuevo, incluido el texto del mensaje con etiqueta que contiene las propiedades de encapsulado.
    
2. Descodificar la secuencia TNEF de los datos adjuntos adecuados.
    
3. Descodificar cualquier otros datos adjuntos y escribir nuevos datos adjuntos de MAPI en un mensaje.
    
4. Abra la secuencia TNEF para descodificar el uso de la función [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Utilice el método [ITnef::ExtractProps](itnef-extractprops.md) para descodificar la secuencia TNEF y escribir las propiedades encapsuladas en el nuevo mensaje. Las propiedades codificadas que son duplicados de las propiedades nonencoded sobrescribirán las propiedades nonencoded cuando se descodificación las propiedades codificadas. 
    
6. Use el método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para analizar el texto del mensaje para recuperar las posiciones de los datos adjuntos de las etiquetas en el texto del mensaje. 
    

