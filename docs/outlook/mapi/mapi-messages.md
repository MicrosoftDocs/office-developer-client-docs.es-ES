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
  
Los mensajes son objetos MAPI que se transmiten de una aplicación cliente a otra a través de la cola MAPI y los proveedores de servicios a través de un sistema de mensajería. Casi todos los componentes de MAPI funcionan con mensajes. Los clientes permiten a los usuarios crear, guardar, enviar y eliminar mensajes además de copiarlos y moverlos de una carpeta a otra. Los proveedores de almacén de mensajes son responsables de la administración de mensajes y de entregar mensajes a la cola MAPI o a un proveedor de transporte. La cola MAPI mueve los mensajes a un proveedor de transporte adecuado, mientras que los proveedores de transporte controlan la entrega y recepción de mensajes desde y hacia un sistema de mensajería y establecen las propiedades de la opción de destinatario y mensaje. Los proveedores de libretas de direcciones trabajan indirectamente con mensajes y admiten propiedades que describen destinatarios de mensajes.
  
Los mensajes se almacenan en carpetas de un almacén de mensajes, normalmente carpetas creadas en la carpeta raíz de mensajes interpersonales (IPM). Los mensajes normalmente se almacenan en el mismo nivel que las carpetas estándar bandeja de entrada IPM, Elementos enviados, Elementos eliminados y Bandeja de salida, o en niveles inferiores de la jerarquía. Sin embargo, los mensajes también se pueden almacenar fuera del subárbol IPM.
  
Los mensajes creados en el subárbol IPM estándar tienen contenido estándar (es decir, contenido visible para el usuario de una aplicación cliente). Las notas y los informes son ejemplos de mensajes que tienen contenido estándar. Los mensajes también se pueden crear con contenido asociado o con contenidos que no están visibles en el cliente típico. Las carpetas admiten dos tablas de contenido diferentes para contener los diferentes tipos de mensajes: una tabla de contenido estándar para mensajes estándar y una tabla de contenido asociada para los mensajes asociados. Dado que MAPI no establece estándares para el contenido de los mensajes asociados, pueden contener información arbitraria. 
  
Un mensaje puede tener datos adicionales (en forma de archivo, otro mensaje o un objeto OLE) asociados a él. Estos datos adicionales, que se denominan datos adjuntos, aparecen como un icono o, para un mensaje RTF, como un metarchivo en el texto del mensaje. Un mensaje puede tener cero, uno o varios datos adjuntos. Los datos adjuntos siempre se transmiten con el mensaje.
  
Un mensaje que se transmite tiene uno o varios destinatarios (direcciones asociadas a un sistema de mensajería determinado). Algunos destinatarios son entradas de un contenedor que pertenece a un proveedor de libreta de direcciones en el perfil actual; otros destinatarios se crean solo para transmitir el mensaje. Dado que los destinatarios y los datos adjuntos deben tener acceso a través del mensaje con el que están asociados, los destinatarios y los datos adjuntos de un mensaje se conocen como sus subobjetos. 
  
Los proveedores de almacén de mensajes admiten mensajes, datos adjuntos y destinatarios a través de métodos en tres interfaces: 
  
|**Interfaz**|**Descripción**|
|:-----|:-----|
|[IMessage](imessageimapiprop.md) <br/> |Administra datos adjuntos y destinatarios, envía mensajes, establece el estado de lectura.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Crea, copia y mueve mensajes y subcarpetas y administra el estado del mensaje.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Administra las propiedades de datos adjuntos.  <br/> |
   
## <a name="see-also"></a>Vea también



[Desarrollo de aplicaciones de MAPI](mapi-application-development.md)

