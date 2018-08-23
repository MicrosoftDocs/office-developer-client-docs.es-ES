---
title: Elegir una clase de mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c3b486838c6ce2d7fc38d950a4de6f4589767073
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574240"
---
# <a name="choosing-a-message-class"></a>Elegir una clase de mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Tal como se describe en [Las clases de mensaje MAPI](mapi-message-classes.md), las clases de mensajes que son importantes para establecer la relación entre los tipos de mensajes personalizados y, por extensión, entre los servidores del formulario a sí mismos. Afortunadamente, la elección de una cadena de la clase de mensaje es bastante sencillo. La cadena de la clase de mensaje de una clase de mensaje es una cadena arbitraria, pero debe utilizar las siguientes convenciones:
  
- La cadena debe cumplir todas las convenciones que se describen en la documentación de la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)). Lo que es importante, la cadena debe estar compuesto por completo de caracteres ANSI y tener menos de 256 caracteres.
    
- Si su servidor de formulario se deriva de un servidor de formulario existente o es una extensión de un servidor de formulario existente, la cadena de la clase de mensaje se debería formada mediante la adición de un período y otra palabra a la cadena de clase de mensaje del servidor de formulario que se basa el formulario. Por ejemplo, es posible que desee implementar un formulario para volver a programar una reunión, y el formulario se basa en un formulario existente para programar reuniones. Si la cadena de clase de mensaje del formulario de programación de reuniones es "IPM. La reunión", la cadena de la clase de mensaje podría ser"IPM. Meeting.Reschedule".
    
- Si el formulario no se basa en cualquier formulario existente, la cadena de la clase de mensaje aún debe comenzar con puede ser el "IPM." o "IPC". prefijo, dependiendo de si el formulario está pensado para ser recibidos por una persona o por otra aplicación. "IPM." designa un mensaje interpersonal que normalmente termina en la Bandeja de entrada de un usuario y "IPC". designa un mensaje de comunicación entre procesos que no se entrega normalmente a Bandeja de entrada de un usuario.
    
- Si su clase de mensaje está pensada para ser legible, la cadena de la clase de mensaje debe comenzar con "IPM." Una clase de mensaje generalmente se considera legible si se utilizan las propiedades que contienen texto sin formato, HTML, o datos de formato de texto enriquecido (RTF). Si el formulario utiliza la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), que debe usar casi sin duda un "IPM." cadena de la clase de mensaje. Por ejemplo, si va a implementar un formulario de pedidos de compra y la organización requiere que un administrador apruebe los pedidos de compra, la cadena de la clase de mensaje podría ser "IPM. Purchase_Order". Los formularios que están diseñados para utilizar con las carpetas públicas o aplicaciones de carpetas públicas se normalmente consideran interpersonales debido a que se leen por personas, aunque no se abordan realmente a la dirección de correo electrónico de cualquier persona. El prefijo habitual en las clases de mensajes de carpetas públicas es "IPM. POST". 
    
- Si su clase de mensaje está pensada para ser recibidas por otra aplicación, en lugar de por una persona, la cadena de la clase de mensaje debe comenzar con "IPC". Por ejemplo, si va a implementar un formulario que permite a los usuarios suscribirse automáticamente a las listas de distribución de correo, la cadena de la clase de mensaje podría ser "IPC. Suscribirse".
    
- La cadena de la clase de mensaje nunca debe terminar con un punto.
    
La cadena de la clase de mensaje se debe colocar en la sección **[descripción]** del archivo de configuración de formulario, en la entrada de **MessageClass** , similar al siguiente: 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Una vez que haya elegido una cadena de la clase de mensaje adecuado, debe generar un identificador de clase para el mismo. Identificadores de clase se pueden generar con el comando **Crear GUID** que se incluye en Visual Studio. El identificador de clase se debe colocar en la entrada **CLSID** del archivo de configuración de formulario, junto con la entrada **MessageClass** , similar al siguiente: 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
El identificador de clase seguramente será diferente, por supuesto. Para obtener más información, vea [crear un archivo de configuración del formulario](creating-a-form-configuration-file.md).
  
Cuando el formulario está instalado en el equipo del usuario, el proceso de instalación: si es un programa de instalación o algo más, debe realizar una entrada del registro en el **HKEY_CLASSES_ROOT\CLSID\* * sección del registro para el identificador de clase. Esta entrada debe establecerse en la cadena de la clase de mensaje. Por ejemplo, podría crear una entrada del Registro similar a la siguiente para el identificador de clase del ejemplo anterior: 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Para obtener más información, vea [instalar un formulario en una biblioteca](installing-a-form-into-a-library.md).
  
## <a name="see-also"></a>Recursos adicionales



[Desarrollar servidores de formulario MAPI](developing-mapi-form-servers.md)

