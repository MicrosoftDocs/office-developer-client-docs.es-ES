---
title: Clases de mensajes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 64ef2bbb-585c-4908-8ad4-a1c954057e9b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b2ab5d56c53216152a83ca207ff5ba1d53c9049d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412089"
---
# <a name="mapi-message-classes"></a>Clases de mensajes MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cada mensaje tiene una propiedad de clase de **mensaje, PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), que identifica el tipo, propósito o contenido del mensaje. **PR_MESSAGE_CLASS** es una propiedad obligatoria en todos los mensajes nuevos. La clase de un mensaje determina el formulario que se usa para presentar el mensaje al usuario y la carpeta para colocar mensajes entrantes. 
  
Las clases de mensajes distinguen mayúsculas de minúsculas y contienen caracteres ASCII del 32 al 127 y están delimitadas por puntos, pero no pueden terminar con un punto. Cada cadena representa un nivel de subclase y no hay ningún límite en el número de niveles permitidos. 
  
Por ejemplo, la mayoría de los mensajes que las aplicaciones cliente envían y reciben se encuentran en la clase de mensaje **IPM,** una categoría amplia que describe todos los mensajes interpersonales (es decir, los mensajes que un usuario humano debe leer, en lugar de hacerlo mediante programación en un equipo). Los proveedores de almacenamiento de mensajes describen de forma más precisa un mensaje IPM mediante la creación de una subclase **IPM.** La **subclase IPM** hereda las propiedades de la **clase de mensaje IPM.** Las subclases de la **clase IPM** se denominan concatenando otras cadenas de caracteres en el identificador IPM, como **IPM. Nota** para describir un mensaje de nota e **IPM. Contacto** para describir un mensaje de contacto. 
  
Para controlar la visualización y administración de mensajes IPM, los clientes pueden usar un formulario estándar que proporciona MAPI. Para controlar la visualización y administración de nuevas clases de mensajes, usted como desarrollador de aplicaciones cliente tiene dos opciones:
  
1. Puede crear un nuevo formulario mediante el conjunto de interfaces de formulario definidas por MAPI que puede usar un cliente estándar.
    
2. Puede escribir su propio cliente implementando una aplicación completa e independiente. 
    
Aunque los clientes deben establecer la propiedad PR_MESSAGE_CLASS para cada mensaje saliente **en** una subclase de **IPM** o **IPC,** el proveedor de al almacenamiento de mensajes tiene la responsabilidad última de establecerla. Por lo tanto, si un cliente envía un mensaje sin establecer su clase de mensaje, el proveedor del almacén de mensajes lo establece en el valor predeterminado adecuado para el tipo de cliente adecuado. La clase de mensaje predeterminada para los clientes de mensajería interpersonal **es IPM;** La clase de mensaje predeterminada para los clientes de comunicación entre procesos es **IPC**. 
  
Las clases de mensajes tienen una restricción de longitud de 255 caracteres. Sin embargo, las clases de mensajes no deben superar los 127 caracteres para admitir las clases de mensaje usadas en los informes. Las clases de mensaje de informe se basan en la clase del mensaje original, con dos adiciones: un prefijo y un sufijo. El prefijo REPORT indica que el mensaje es un informe y el sufijo indica el tipo de informe: DR (informe de entrega), NDR (informe de no entrega), IPNRN (informe de lectura) o IPNNRN (informe no leído). Tenga en cuenta que estas restricciones de longitud se dan en caracteres; en plataformas que usan un juego de caracteres de doble byte, el recuento de bytes real podría ser mayor. 
  
Los proveedores de almacenamiento de mensajes deben devolver MAPI_E_INVALID_PARAMETER de sus implementaciones de método [IMAPIProp::SetProps](imapiprop-setprops.md) cuando un cliente intenta asignar una cadena que supera el límite permitido para su clase de mensaje. 
  
## <a name="see-also"></a>Consulte también



[Mensajes MAPI](mapi-messages.md)

