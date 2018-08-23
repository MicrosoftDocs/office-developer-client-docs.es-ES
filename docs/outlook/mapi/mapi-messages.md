---
title: Mensajes MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 417c113f-bd98-4515-85d1-09db7fc3a227
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cf7876dacac40420fdedb8b6f55c99efcf56c4f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579938"
---
# <a name="mapi-messages"></a>Mensajes MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los mensajes son objetos MAPI que se transmiten desde una aplicación cliente a otro a través de la cola MAPI y los proveedores de servicios por medio de un sistema de mensajería. Casi todos los componentes en MAPI funciona con los mensajes. Los clientes permiten a los usuarios crear, guardar, enviar y eliminar mensajes además de copiar y mover de una carpeta a otra. Los proveedores de almacén de mensajes son responsables de la administración de mensajes y de entrega de mensajes a la cola MAPI o un proveedor de transporte. La cola MAPI mueve los mensajes a un proveedor de transporte adecuados, mientras que los proveedores de transporte controlen la entrega y la recepción de mensajes a y desde un sistema de mensajería y establezca destinatario y mensaje propiedades de opción. Los proveedores de la libreta de direcciones indirectamente trabajar con mensajes, compatibilidad con las propiedades que describen a los destinatarios del mensaje.
  
Los mensajes se almacenan en las carpetas a lo largo de un almacén de mensajes, normalmente, las carpetas creadas en la carpeta raíz de mensajes interpersonales (IPM). Los mensajes se almacenan normalmente en el mismo nivel que la Bandeja de entrada IPM estándar, elementos enviados, elementos eliminados y las carpetas Bandeja de salida, o en los niveles inferiores en la jerarquía. Sin embargo, también se pueden almacenar mensajes fuera del subárbol IPM.
  
Los mensajes creados en el subárbol IPM estándar tienen contenido estándar (es decir, contenido que está visible para el usuario de una aplicación de cliente). Notas y los informes son ejemplos de los mensajes que tienen contenido estándar. También se pueden crear mensajes con asociados, o contenido que no está visible en el cliente típico. Las carpetas admiten dos tablas de contenido diferente para retener los diferentes tipos de mensajes: un estándar de contenido de la tabla para mensajes estándar y una tabla de contenido asociada para los mensajes asociados. Debido a que MAPI no establece los estándares para el contenido de los mensajes asociados, que pueden contener información arbitraria. 
  
Datos adicionales que puede tener un mensaje, con el formato de un archivo, otro mensaje o un objeto OLE, asociados con ella. Estos datos adicionales, que se llama a un archivo adjunto, aparecen como un icono o, para un mensaje RTF, como un metarchivo en el texto del mensaje. Un mensaje puede tener cero, uno o muchos datos adjuntos. Los datos adjuntos siempre se transmiten con el mensaje.
  
Un mensaje que se transmite tiene uno o más destinatarios (direcciones que están asociados con un sistema de mensajería determinado). Algunos destinatarios son las entradas de un contenedor que pertenece a un proveedor de la libreta de direcciones en el perfil actual; otros destinatarios se crean sólo para transmitir el mensaje. Debido a que deben tener acceso a los destinatarios y los datos adjuntos a través del mensaje con la que se asocian, los destinatarios y los datos adjuntos de un mensaje se conocen como los subobjetos. 
  
Los proveedores de almacén de mensajes admiten los mensajes, datos adjuntos y los destinatarios a través de métodos en tres interfaces: 
  
|**Interfaz**|**Descripción**|
|:-----|:-----|
|[IMessage](imessageimapiprop.md) <br/> |Administra los datos adjuntos y los destinatarios, envía mensajes, Establece el estado de lectura.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Crea, copia y mueve los mensajes y subcarpetas y administra el estado del mensaje.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Administra las propiedades de los datos adjuntos.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Desarrollo de aplicaciones de MAPI](mapi-application-development.md)

