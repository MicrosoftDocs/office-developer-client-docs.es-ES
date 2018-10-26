---
title: Compatibilidad con formularios y vistas de s�lo lectura de los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 52aebb53f2bc0e5af72f2da47b91ba2806d7f709
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563355"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a>Compatibilidad con formularios y vistas de s�lo lectura de los almacenes de mensajes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Si el proveedor de almac�n de mensajes permite permiso de solo lectura para el mecanismo de almacenamiento subyacente, las aplicaciones cliente y el Administrador de formularios MAPI se puedan realizar determinadas tareas. En concreto, los clientes no podr�n agregar o modificar vistas personalizadas y Administrador de formularios MAPI no podr�n instalar formularios en las tablas de contenido asociada de carpetas del almac�n.
  
Para muchos de los almacenes de mensaje de s�lo lectura, que no sea un problema. Si ese es el caso, el proveedor de almacenamiento de mensajes no es necesario admitir en todas las tablas de contenido asociada. Sin embargo, si el proveedor de almacenes de mensaje debe ser de solo lectura y tambi�n debe admitir un conjunto predefinido de vistas o formularios, tendr� que admiten las tablas de contenido asociada.
  
La estrategia m�s com�n para hacerlo, ya que los clientes y el Administrador de formularios MAPI no pueden instalar las vistas o formularios en el mensaje almac�n ellos mismos, es para el proveedor de almacenamiento de mensajes para codificar ellos en el almac�n de mensajes. Esto significa que la tabla de contenido asociados o tablas que contienen los formularios o vistas existan en el almac�n de mensajes cuando se crea, antes de cualquier cliente o la MAPI formulario administrador nunca acceder a �l. A continuaci�n, cuando un cliente solicita una tabla de contenido asociada para obtener vistas personalizadas de un formulario o el Administrador de formularios MAPI solicita una tabla de contenido asociada al inicio de un formulario, el proveedor de almacenamiento de mensajes puede proporcionar uno. 
  
Este requisito que las tablas de contenido asociado se crea y rellena cuando se crea el propio almac�n de mensajes implica que tendr� su proveedor de almacenamiento de mensajes obtener informaci�n sobre el formato de los mensajes especiales que los clientes y la MAPI manager se usa para almacenar los formularios y vistas de formulario. �Qu� son los formatos depender� en el cliente y el Administrador de formularios MAPI se usan, por lo que no se puede proporcionar una descripci�n de ellos de aqu�.
  
## <a name="see-also"></a>Vea tambi�n



[Almacenes de mensaje de s�lo lectura](read-only-message-stores.md)

