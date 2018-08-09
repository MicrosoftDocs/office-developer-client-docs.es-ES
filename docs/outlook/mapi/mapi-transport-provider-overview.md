---
title: Información general sobre el proveedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 11cd1040bb228d789248a89184572b87cd1688ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818236"
---
# <a name="mapi-transport-provider-overview"></a>Información general sobre el proveedor de transporte MAPI

  
  
**Hace referencia a**: Outlook 
  
Los proveedores de transporte controlan la recepción y transmisión de mensajes e implementan la seguridad, si es necesario. También se ocupe de cualquier preprocesamiento necesarios y tareas de posprocesamiento. No hay proveedor de transporte normalmente, uno para cada sistema de mensajería activa.
  
Aplicaciones cliente se comunican con el proveedor de transporte a través de un proveedor de almacén de mensajes. 
  
Registran los proveedores de transporte con MAPI para manejar tipos específicos de una o varias de las entradas de destinatarios. Cuando un mensaje está listo para ser enviado, MAPI debe determinar qué proveedor de transporte debe controlar la transmisión. Según el tipo de destinatario, MAPI incluso puede recurrir a más de un proveedor de transporte. Si un proveedor de transporte disponible es el único que puede controlar al destinatario, la transmisión del mensaje se se pospuso hasta que se puede restablecer una conexión con el proveedor.
  
Algunos sistemas de mensajería son los sistemas seguros; todos los usuarios potenciales tienen que escribir un conjunto de credenciales válidas para obtener acceso. MAPI impide el acceso no autorizado a estos sistemas de mensajería seguros con el proveedor de transporte validar credenciales en tiempo de inicio de sesión. 
  

