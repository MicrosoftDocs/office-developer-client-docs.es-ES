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
ms.openlocfilehash: f1d1895cc6f9e65929781cb0e966873d2bce197c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423380"
---
# <a name="mapi-messages"></a>Mensajes MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los mensajes son objetos MAPI que se transmiten de una aplicación cliente a otra a través de la cola MAPI y los proveedores de servicios por medio de un sistema de mensajería. Casi todos los componentes de MAPI funcionan con los mensajes. Los clientes permiten a los usuarios crear, guardar, enviar y eliminar mensajes, además de copiarlos y moverlos de una carpeta a otra. Los proveedores de almacenamiento de mensajes son responsables de la administración de mensajes y de la entrega de mensajes a la cola MAPI o a un proveedor de transporte. La cola MAPI mueve los mensajes a un proveedor de transporte adecuado, mientras que los proveedores de transporte administran la entrega y la recepción de mensajes en y desde un sistema de mensajería y establecen las propiedades de las opciones de destinatario y mensaje. Los proveedores de libreta de direcciones trabajan de forma indirecta con los mensajes y admiten propiedades que describen los destinatarios del mensaje.
  
Los mensajes se almacenan en carpetas en un almacén de mensajes, normalmente carpetas creadas en la carpeta raíz del mensaje interpersonal (IPM). Normalmente, los mensajes se almacenan en el mismo nivel que la bandeja de entrada IPM estándar, elementos enviados, elementos eliminados y carpetas de la bandeja de salida, o en niveles inferiores de la jerarquía. Sin embargo, los mensajes también se pueden almacenar fuera del subárbol IPM.
  
Los mensajes creados en el subárbol estándar de IPM tienen contenido estándar (es decir, contenido que es visible para el usuario de una aplicación de cliente). Las notas e informes son ejemplos de mensajes que tienen contenido estándar. Los mensajes también se pueden crear con contenido asociado o contenido que no es visible en el cliente típico. Las carpetas admiten dos tablas de contenido diferentes para contener los distintos tipos de mensajes: una tabla de contenido estándar para los mensajes estándar y una tabla de contenido asociada para los mensajes asociados. Debido a que MAPI no establece estándares para el contenido de los mensajes asociados, puede contener información arbitraria. 
  
Un mensaje puede tener datos adicionales (en forma de un archivo, otro mensaje o un objeto OLE) asociados a él. Estos datos adicionales, que se denominan datos adjuntos, se muestran como un icono o, en el caso de un mensaje RTF, como un metarchivo en el texto del mensaje. Un mensaje puede tener cero, uno o muchos datos adjuntos. Los datos adJuntos siempre se transmiten con el mensaje.
  
Un mensaje que se transmite tiene uno o más destinatarios (direcciones asociadas con un sistema de mensajería en particular). Algunos destinatarios son entradas en un contenedor que pertenece a un proveedor de la libreta de direcciones en el perfil actual; los demás destinatarios solo se crean para transmitir el mensaje. Como se debe tener acceso a los destinatarios y datos adjuntos a través del mensaje con el que están asociados, los destinatarios y los datos adjuntos de un mensaje se conocen como sus subobjetos. 
  
Los proveedores de almacenamiento de mensajes admiten mensajes, datos adjuntos y destinatarios mediante métodos en tres interfaces: 
  
|**Interfaz**|**Descripción**|
|:-----|:-----|
|[IMessage](imessageimapiprop.md) <br/> |Administra datos adjuntos y destinatarios, envía mensajes y establece el estado de lectura.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Crea, copia y mueve mensajes y subcarpetas, y administra el estado de los mensajes.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Administra las propiedades de datos adjuntos.  <br/> |
   
## <a name="see-also"></a>Ver también



[Desarrollo de aplicaciones de MAPI](mapi-application-development.md)

