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
  
Como se describe en [las clases de mensajes MAPI](mapi-message-classes.md), las clases de mensajes son importantes para establecer la relación entre los tipos de mensajes personalizados y, por extensión, entre los propios servidores de formularios. Afortunadamente, la elección de una cadena de clase de mensaje es bastante sencilla. La cadena de clase de mensaje de una clase de mensaje es una cadena arbitraria, pero debe usar las siguientes convenciones:
  
- La cadena debe cumplir todas las convenciones descritas en la documentación de la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)). Importante, la cadena debe estar formada solo por caracteres ANSI y tener menos de 256 caracteres de longitud.
    
- Si el servidor de formularios se deriva de un servidor de formularios existente o es una extensión de un servidor de formularios existente, la cadena de clase de mensaje se debe formar agregando un punto y otra palabra a la cadena de clase de mensaje del servidor de formularios en el que se basa el formulario. Por ejemplo, es posible que desee implementar un formulario para volver a programar una reunión y el formulario se base en un formulario existente para programar reuniones. Si la cadena de clase de mensaje del formulario de programación de reuniones es "IPM. Reunión ", la cadena de clase de mensaje podría ser" IPM. Reunión. reprogramación ".
    
- Si el formulario no se basa en ningún formulario existente, la cadena de la clase de mensaje debería comenzar con "IPM". o "IPC". , en función de si el formulario está destinado a ser recibido por una persona o por otra aplicación. "IPM". designa un mensaje interpersonal que normalmente termina en la bandeja de entrada de un usuario y "IPC". designa un mensaje de comunicación entre procesos que normalmente no se entrega en la bandeja de entrada de un usuario.
    
- Si la clase de mensaje está pensada para ser legible para el usuario, la cadena de clase de mensaje debería comenzar con "IPM". Una clase de mensaje suele considerarse legible para el usuario si usa propiedades que contienen datos de texto sin formato, HTML o formato de texto enriquecido (RTF). Si el formulario utiliza la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), debería usar con certeza un "IPM". cadena de clase de mensaje. Por ejemplo, si está implementando un formulario para pedidos de compra y su organización requiere que el administrador apruebe los pedidos de compra, la cadena de clase de mensaje podría ser "IPM. Purchase_Order ". Los formularios que se diseñan para usarse con carpetas públicas o con aplicaciones de carpetas públicas suelen considerarse interpersonales porque son leídos por los usuarios, aunque en realidad no se les dirige a la dirección de correo electrónico de ninguna persona. El prefijo típico para las clases de mensajes de carpeta pública es "IPM. Post ". 
    
- Si la clase de mensaje está pensada para que la reciba otra aplicación en lugar de una persona, la cadena de clase de mensaje debería comenzar con "IPC". Por ejemplo, si está implementando un formulario que permite a los usuarios suscribirse automáticamente a listas de correo, la cadena de clase de mensaje podría ser "IPC. Suscribirse ".
    
- La cadena de clase de mensaje nunca debe terminar con un punto.
    
La cadena de clase de mensaje se debe colocar en la sección **[Descripción]** del archivo de configuración de formulario, en la entrada **MessageClass** , similar a la siguiente: 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Una vez que haya elegido una cadena de clase de mensaje adecuada, debe generar un identificador de clase para ella. Los identificadores de clase se pueden generar con el comando **Create GUID** que se incluye en Visual Studio. El identificador de clase debe colocarse en la entrada **CLSID** del archivo de configuración de formulario, junto con la entrada **MessageClass** , similar a la siguiente: 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
Por supuesto, es muy probable que el identificador de clase sea diferente. Para obtener más información, vea [crear un archivo de configuración de formulario](creating-a-form-configuration-file.md).
  
Cuando se instala el formulario en el equipo de un usuario, el proceso de instalación, ya sea un programa de instalación o de otro tipo, debe crear una entrada del registro en la sección **HKEY_CLASSES_ROOT\CLSID\* * del registro para el identificador de clase. Esta entrada debe establecerse en la cadena de clase de mensaje. Por ejemplo, podría crear una entrada del registro similar a la siguiente para el identificador de clase de ejemplo anterior: 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Para obtener más información, vea [instalar un formulario en una biblioteca](installing-a-form-into-a-library.md).
  
## <a name="see-also"></a>Ver también



[Desarrollar servidores de formulario MAPI](developing-mapi-form-servers.md)

