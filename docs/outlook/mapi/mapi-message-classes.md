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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345902"
---
# <a name="mapi-message-classes"></a>Clases de mensajes MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cada mensaje tiene una propiedad de clase de mensaje, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), que identifica el tipo, propósito o contenido del mensaje. **PR_MESSAGE_CLASS** es una propiedad necesaria en todos los mensajes nuevos. La clase de un mensaje determina el formulario que se usa para presentar el mensaje al usuario y la carpeta para colocar los mensajes entrantes. 
  
Las clases de mensaje distinguen entre mayúsculas y minúsculas y las cadenas de caracteres que contienen caracteres ASCII 32 a 127 y están delimitadas por puntos, pero no pueden terminar con un punto. Cada cadena representa un nivel de subclases y no hay ningún límite en el número de niveles permitidos. 
  
Por ejemplo, la mayoría de los mensajes que envían y reciben las aplicaciones cliente se dividen en la clase de mensaje **IPM** , una amplia categoría que describe todos los mensajes interpersonales (es decir, los mensajes que se van a leer por un usuario humano, en lugar de que mediante programación un equipo). Los proveedores de almacenamiento de mensajes describen con más precisión un mensaje IPM creando una subclase **IPM** . La subclase **IPM** hereda las propiedades de la clase de mensaje **IPM** . Las subclases de la clase **IPM** se denominan concatenando otras cadenas de caracteres en el identificador IPM, como **IPM. Nota** para describir un mensaje de nota e **IPM. Contacto** para describir un mensaje de contacto. 
  
Para controlar la presentación y la administración de mensajes IPM, los clientes pueden usar un formulario estándar que proporciona MAPI. Para controlar la visualización y la administración de nuevas clases de mensajes, como desarrollador de aplicaciones cliente tiene dos opciones:
  
1. Puede crear un nuevo formulario con el conjunto de interfaces de formulario definidas por MAPI que puede usar un cliente estándar.
    
2. Puede escribir su propio cliente implementando una aplicación independiente completa. 
    
Aunque los clientes deberían establecer la propiedad **PR_MESSAGE_CLASS** para cada mensaje saliente en una subclase de **IPM** o **IPC**, el proveedor de almacenamiento de mensajes tiene la responsabilidad final de establecerla. Por lo tanto, si un cliente envía un mensaje sin establecer su clase de mensaje, el proveedor de almacenamiento de mensajes lo establece en el valor predeterminado adecuado para el tipo de cliente adecuado. La clase de mensaje predeterminada para los clientes de mensajería interpersonal es **IPM**; la clase de mensaje predeterminada para los clientes de comunicación entre procesos es **IPC**. 
  
Las clases de mensaje tienen una restricción de longitud de 255 caracteres. Sin embargo, las clases de mensaje no deben superar los 127 caracteres para admitir las clases de mensaje que se usan en los informes. Las clases de mensaje de informe se basan en la clase del mensaje original, con dos adiciones: un prefijo y un sufijo. El informe de prefijo indica que el mensaje es un informe y el sufijo indica el tipo de informe: DR (informe de entrega), NDR (informe de no entrega), IPNRN (leer informe) o IPNNRN (nonread Report). Tenga en cuenta que estas restricciones de longitud se dan en caracteres; en las plataformas que usan un juego de caracteres de doble byte, el recuento de bytes real puede ser superior. 
  
Los proveedores de almacenamiento de mensajes deben devolver MAPI_E_INVALID_PARAMETER de sus implementaciones del método [IMAPIProp:: SetProps](imapiprop-setprops.md) cuando un cliente intenta asignar una cadena que supera el límite permitido para su clase de mensaje. 
  
## <a name="see-also"></a>Vea también



[Mensajes MAPI](mapi-messages.md)

