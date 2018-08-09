---
title: Implementación tablas puntuales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b72b8658270a8e007123df3ead01168208b8d1b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817692"
---
# <a name="implementing-one-off-tables"></a>Implementación tablas puntuales

**Hace referencia a**: Outlook 
  
El proveedor podría implementar una o varias tablas de uso único. Una tabla de uso único es una lista de resumen de uso único plantillas que se usan para crear a destinatarios, ya sea directamente en un contenedor o en la lista de destinatarios de un mensaje saliente. Una plantilla de uso único es un emplean de los usuarios del formulario para escribir datos relevantes para un determinado tipo de dirección. Cuando el usuario es terminado de trabajar con la plantilla, su proveedor crea el destinatario nuevo y lo agrega al mensaje. Normalmente, cada plantilla controla un tipo de una sola dirección. Sin embargo, es posible para una plantilla controlar varios tipos o para varias plantillas controlar el mismo tipo. 
  
El proveedor debe admitir el método **OpenEntry** para cada plantilla que incluye en la tabla de uso único. La implementación de **OpenEntry** debe recuperar una tabla para mostrar para la plantilla. MAPI utiliza la tabla de presentación para que la plantilla sea visible para el usuario. 
  
Aunque la mayoría de las filas de tablas de uso único representa plantillas, algunas de las filas se pueden usar para clasificar o de grupo, las plantillas. Representa una fila en una tabla de uso único o no una plantilla se indica mediante el valor de la columna **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)). Las filas que representan las plantillas tienen la columna PR_SELECTABLE establecida en TRUE; las filas que no se representan las plantillas tienen establecido en FALSE.
  
MAPI define tres tipos de tablas de uso único:
  
- Una tabla de uso único que refleja las plantillas que admite un contenedor individual
    
- Una tabla de uso único que refleja todas las plantillas que admita el proveedor 
    
- Una tabla de uso único que refleja todas las plantillas de todos los proveedores en el perfil de admitan plus algunas que es compatible con MAPI
    
Los dos primeros tipos se implementan los proveedores que admiten a los destinatarios de creación, ya sea en un mensaje o en un contenedor. Su proveedor puede incluir el mismo conjunto o un conjunto diferente de plantillas en sus tablas de uso único. La diferencia principal entre los dos tipos es que la tabla de proveedor debe incluir plantillas para la creación de los destinatarios que se pueden usar en los mensajes salientes y su tabla de contenedor debe incluir plantillas para la creación de los destinatarios que se agregarán a su contenedor. Un contenedor sólo puede admitir un conjunto limitado de plantillas, pero la tabla de uso único proveedor debe incluir todas las plantillas del proveedor admite.
  
El tercer tipo de tabla de uso único se implementa mediante MAPI; proveedores de obtienen acceso a ella mediante una llamada a [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). En la tabla de uso único de MAPI es la unión de todas las tablas de proveedor; incluye todas las plantillas que admite cada proveedor en el perfil. También incluye plantillas compatibles con MAPI. Puede utilizar esta tabla en lugar de la tabla que solicitó para un contenedor en el proveedor. Sin embargo, las plantillas de esta tabla también se pueden usar para la creación de destinatarios para los mensajes salientes.
  

