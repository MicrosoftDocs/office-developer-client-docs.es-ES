---
title: Elección de una clase de mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 279df7f07c8c8b66347488c6224d04f70292e968
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428056"
---
# <a name="choosing-a-message-class"></a>Elección de una clase de mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Como se describe en las clases de mensajes [MAPI,](mapi-message-classes.md)las clases de mensajes son importantes para establecer la relación entre los tipos de mensajes personalizados y, por extensión, entre los propios servidores de formulario. Afortunadamente, elegir una cadena de clase de mensaje es bastante sencillo. La cadena de clase de mensaje de una clase de mensaje es una cadena arbitraria, pero debe usar las siguientes convenciones:
  
- La cadena debe cumplir todas las convenciones descritas en la documentación para **la propiedad PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)). Es importante destacar que la cadena debe estar compuesta por completo por caracteres ANSI y tener menos de 256 caracteres.
    
- Si el servidor de formulario se deriva de un servidor de formulario existente o es una extensión de un servidor de formulario existente, la cadena de clase de mensaje debe formarse agregando un punto y otra palabra a la cadena de clase de mensaje del servidor de formulario en el que se basa el formulario. Por ejemplo, puede que desee implementar un formulario para reprogramar una reunión y el formulario se basa en un formulario existente para programar reuniones. Si la cadena de clase de mensaje del formulario de programación de reuniones es "IPM. Reunión", la cadena de clase de mensaje podría ser "IPM. Meeting.Reschedule".
    
- Si el formulario no se basa en ningún formulario existente, la cadena de clase de mensaje debe comenzar con el "IPM". o "IPC". en función de si el formulario está pensado para ser recibido por una persona o por otra aplicación. "IPM". designa un mensaje interpersonal que normalmente termina en la Bandeja de entrada de un usuario y "IPC". designa un mensaje de comunicación entre procesos que normalmente no se entrega a la Bandeja de entrada de un usuario.
    
- Si la clase de mensaje está pensada para ser legible para el usuario, la cadena de clase de mensaje debe comenzar con "IPM". Por lo general, una clase de mensaje se considera legible para las personas si usa propiedades que contienen datos de texto sin formato, HTML o formato de texto enriquecido (RTF). Si el formulario usa la **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), casi con toda seguridad debe usar un "IPM". cadena de clase de mensaje. Por ejemplo, si va a implementar un formulario para los pedidos de compra y su organización requiere que un administrador apruebe los pedidos de compra, la cadena de clase de mensaje podría ser "IPM. Purchase_Order". Los formularios diseñados para su uso con carpetas públicas o aplicaciones de carpetas públicas suelen considerarse interpersonales, ya que los leen las personas aunque no se dirigen realmente a la dirección de correo electrónico de ninguna persona. El prefijo típico para las clases de mensajes de carpetas públicas es "IPM. Post". 
    
- Si la clase de mensaje está pensada para ser recibida por otra aplicación en lugar de por una persona, la cadena de clase de mensaje debe comenzar con "IPC". Por ejemplo, si está implementando un formulario que permite a los usuarios suscribirse automáticamente a listas de correo, la cadena de clase de mensaje podría ser "IPC. Suscribirse".
    
- La cadena de clase de mensaje nunca debe terminar con un punto.
    
La cadena de clase de mensaje debe colocarse en la sección **[Descripción]** del archivo de configuración del formulario, en la **entrada MessageClass,** similar a la siguiente: 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Después de elegir una cadena de clase de mensaje adecuada, debe generar un identificador de clase para ella. Los identificadores de clase se pueden generar con el comando **Create GUID** que se incluye en Visual Studio. El identificador de clase debe incluirse en la entrada **CLSID** del archivo de configuración del formulario, junto con la entrada **MessageClass,** similar a la siguiente: 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
Por supuesto, el identificador de clase será casi distinto. Para obtener más información, vea [Crear un archivo de configuración de formulario.](creating-a-form-configuration-file.md)
  
Cuando el formulario se instala en el equipo de un usuario, el proceso de instalación (ya sea un programa de instalación o cualquier otra cosa) debe crear una entrada del Registro en la sección **HKEY_CLASSES_ROOT\CLSID\** del Registro para el identificador de clase. Esta entrada debe establecerse en la cadena de clase de mensaje. Por ejemplo, crearía una entrada del Registro similar a la siguiente para el identificador de clase de ejemplo anterior: 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Para obtener más información, vea [Instalar un formulario en una biblioteca.](installing-a-form-into-a-library.md)
  
## <a name="see-also"></a>Consulte también



[Desarrollo de servidores de formulario MAPI](developing-mapi-form-servers.md)

