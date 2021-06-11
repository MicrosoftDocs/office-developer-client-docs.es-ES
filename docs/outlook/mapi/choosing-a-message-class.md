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
ms.openlocfilehash: 279df7f07c8c8b66347488c6224d04f70292e968
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428056"
---
# <a name="choosing-a-message-class"></a>Elegir una clase de mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Como se describe en Clases de mensajes [MAPI,](mapi-message-classes.md)las clases de mensajes son importantes para establecer la relación entre los tipos de mensajes personalizados y, por extensión, entre los propios servidores de formulario. Afortunadamente, elegir una cadena de clase de mensaje es bastante sencillo. La cadena de clase de mensaje de una clase de mensaje es una cadena arbitraria, pero debe usar las convenciones siguientes:
  
- La cadena debe satisfacer todas las convenciones descritas en la documentación de la **propiedad PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)). Es importante destacar que la cadena debe estar compuesta por completo de caracteres ANSI y tener menos de 256 caracteres de longitud.
    
- Si el servidor de formularios deriva de un servidor de formulario existente o es una extensión de un servidor de formulario existente, la cadena de clase de mensaje debe formarse agregando un punto y otra palabra a la cadena de clase de mensaje del servidor de formulario en el que se basa el formulario. Por ejemplo, es posible que desee implementar un formulario para reprogramar una reunión y el formulario se basa en un formulario existente para programar reuniones. Si la cadena de clase de mensaje del formulario de programación de reuniones es "IPM. Meeting", la cadena de clase de mensaje podría ser "IPM. Meeting.Reschedule".
    
- Si el formulario no se basa en ningún formulario existente, la cadena de clase de mensaje debe comenzar por "IPM". o "IPC". prefijo, en función de si el formulario está pensado para ser recibido por una persona o por otra aplicación. "IPM". designa un mensaje interpersonal que suele terminar en la Bandeja de entrada de un usuario y "IPC". designa un mensaje de comunicación entre procesos que normalmente no se entrega a la Bandeja de entrada de un usuario.
    
- Si la clase de mensaje está diseñada para ser legible, la cadena de clase de mensaje debe comenzar por "IPM". Por lo general, una clase de mensaje se considera legible para personas si usa propiedades que contienen datos de texto sin formato, HTML o formato de texto enriquecido (RTF). Si el formulario usa la **propiedad PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), casi seguro que debe usar un "IPM". cadena de clase message. Por ejemplo, si va a implementar un formulario para pedidos de compra y su organización requiere que un administrador apruebe los pedidos de compra, la cadena de clase de mensaje podría ser "IPM. Purchase_Order". Los formularios diseñados para su uso con carpetas públicas o aplicaciones de carpetas públicas suelen considerarse interpersonales porque son leídos por las personas, aunque en realidad no están dirigidos a la dirección de correo electrónico de ninguna persona. El prefijo típico de las clases de mensajes de carpetas públicas es "IPM. Post". 
    
- Si la clase de mensaje está diseñada para ser recibida por otra aplicación en lugar de por una persona, la cadena de clase de mensaje debe comenzar por "IPC". Por ejemplo, si va a implementar un formulario que permite a las personas suscribirse automáticamente a listas de correo, la cadena de clase de mensaje podría ser "IPC. Suscribirse".
    
- La cadena de clase de mensaje nunca debe terminar con un punto.
    
La cadena de clase de mensaje debe colocarse en la sección **[Descripción]** del archivo de configuración del formulario, en la **entrada MessageClass,** de forma similar a la siguiente: 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Después de elegir una cadena de clase de mensaje adecuada, debe generar un identificador de clase para ella. Los identificadores de clase se pueden generar con el **comando Create GUID** que se incluye en Visual Studio. El identificador de clase debe colocarse en la entrada **CLSID** del archivo de configuración del formulario, junto con la **entrada MessageClass,** de forma similar a la siguiente: 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
Por supuesto, el identificador de clase será casi distinto. Para obtener más información, vea [Creating a Form Configuration File](creating-a-form-configuration-file.md).
  
Cuando el formulario se instala en el equipo de un usuario, el proceso de instalación (ya sea un programa de instalación o cualquier otra cosa) debe realizar una entrada del Registro en la sección **HKEY_CLASSES_ROOT\CLSID\** del registro para el identificador de clase. Esta entrada debe establecerse en la cadena de clase de mensaje. Por ejemplo, crearía una entrada del Registro similar a la siguiente para el identificador de clase de ejemplo anterior: 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Para obtener más información, vea [Installing a Form into a Library](installing-a-form-into-a-library.md).
  
## <a name="see-also"></a>Vea también



[Desarrollo de servidores de formulario MAPI](developing-mapi-form-servers.md)

