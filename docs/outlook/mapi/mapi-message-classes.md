---
title: Clases de mensaje MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 64ef2bbb-585c-4908-8ad4-a1c954057e9b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 27b81c0939aa3e880f3998d33f4717c51bdbe681
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818155"
---
# <a name="mapi-message-classes"></a>Clases de mensaje MAPI

  
  
**Hace referencia a**: Outlook 
  
Cada mensaje tiene una propiedad de clase de mensaje, **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), que identifica el tipo, el propósito o el contenido del mensaje. **PR_MESSAGE_CLASS** es una propiedad necesaria en todos los mensajes nuevos. Clase de un mensaje determina el formulario que se usa para presentar el mensaje al usuario y a la carpeta para colocar los mensajes entrantes. 
  
Las clases de mensajes son cadenas de caracteres entre mayúsculas y minúsculas que contienen caracteres ASCII 32 a 127 y están delimitadas por puntos, pero no pueden terminar con un punto. Cada cadena representa un nivel de creación de subclases, y no hay ningún límite para el número de niveles permitido. 
  
Por ejemplo, la clase mayoría de los mensajes que las aplicaciones cliente de envían y reciben entran en el mensaje **IPM** , una categoría amplia que describe todos los mensajes interpersonales (es decir, los mensajes que están diseñados para ser leído por un usuario humano, en lugar de mediante programación por un equipo). Los proveedores de almacén de mensajes describen con más precisión un mensaje IPM mediante la creación de una subclase **IPM** . La subclase **IPM** hereda las propiedades de la clase de mensaje **IPM** . Se denominan subclases de la clase **IPM** concatenando otras cadenas de caracteres en el identificador IPM, como **IPM. Nota** para describir un mensaje de nota y **IPM. Póngase en contacto con** para describir un mensaje de contacto. 
  
Para controlar la presentación y la administración de mensajes de IPM, los clientes pueden utilizar un formulario estándar que proporciona de MAPI. Para controlar la presentación y la administración de nuevas clases de mensaje, como desarrollador de aplicaciones cliente tiene dos opciones:
  
1. Puede crear un nuevo formulario utilizando el conjunto de interfaces de formulario MAPI definido por el que se puede usar un cliente estándar.
    
2. Puede escribir su propios cliente mediante la implementación completa, aplicación independiente. 
    
Aunque los clientes deben establecer la propiedad **PR_MESSAGE_CLASS** para todos los mensajes salientes a una subclase de **IPM** o **IPC**, el proveedor de almacén de mensajes tiene la responsabilidad de establecerla. Por lo tanto, si un cliente envía un mensaje sin establecer su clase de mensaje, el proveedor de almacén de mensajes lo establece en el valor predeterminado adecuado para el tipo adecuado de cliente. La clase de mensaje predeterminada para clientes de mensajería interpersonales es **IPM**; la clase de mensaje predeterminada para los clientes de comunicación entre procesos es **IPC**. 
  
Las clases de mensajes tienen una restricción de longitud de 255 caracteres. Sin embargo, las clases de mensajes no deben superar los 127 caracteres para admitir las clases de mensaje que se usan en los informes. Las clases de mensajes de informe se basan en la clase del mensaje original, con dos adiciones: un prefijo y un sufijo. El prefijo de informe indica que el mensaje es un informe, y el sufijo indica el tipo de informe: recuperación ante desastres (informe de entrega), NDR (informe de no entrega), IPNRN (lea el informe) o IPNNRN (informe nonread). Tenga en cuenta que se conceden estas restricciones de longitud en caracteres; en plataformas que usan un conjunto de caracteres de doble byte, el número de bytes real puede ser mayor. 
  
Los proveedores de almacén de mensajes deben devolver MAPI_E_INVALID_PARAMETER desde sus implementaciones de método [IMAPIProp::SetProps](imapiprop-setprops.md) cuando un cliente intenta asignar una cadena que supera el límite permitido para su clase de mensaje. 
  
## <a name="see-also"></a>Vea también



[Mensajes MAPI](mapi-messages.md)

