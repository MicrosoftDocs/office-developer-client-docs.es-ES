---
title: Implementación de tablas de un solo uso
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c29feae84d81874988997409fd229b042a701640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310132"
---
# <a name="implementing-one-off-tables"></a>Implementación de tablas de un solo uso

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Es posible que el proveedor implemente una o más tablas de un solo uso. Una tabla de uso único es una lista resumida de las plantillas de uso único utilizadas para crear destinatarios, ya sea directamente en un contenedor o en la lista de destinatarios de un mensaje saliente. Una plantilla única es un formulario que los usuarios emplean para escribir los datos relevantes para un tipo determinado de dirección. Cuando el usuario termina de trabajar con la plantilla, el proveedor crea el nuevo destinatario y lo agrega al mensaje. Normalmente, cada plantilla administra un solo tipo de dirección. Sin embargo, es posible que una plantilla controle varios tipos o que varias plantillas controlen el mismo tipo. 
  
El proveedor debe admitir el método **OpenEntry** para cada plantilla que incluya en la tabla de uso único. La implementación de **OpenEntry** debe recuperar una tabla de presentación para la plantilla. MAPI usa la tabla de presentación para hacer que la plantilla esté visible para el usuario. 
  
Aunque la mayoría de las filas de las tablas de uso único representan plantillas, se pueden usar algunas de las filas para categorizar o agrupar las plantillas. Si una fila de una tabla de uso único o no representa una plantilla se indica mediante el valor de su columna **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)). Las filas que representan plantillas tienen la columna PR_SELECTABLE establecida en TRUE; las filas que no representan plantillas tienen el valor FALSE.
  
MAPI define tres tipos de tablas de un solo uso:
  
- Una tabla única que refleje las plantillas que admite un contenedor individual
    
- Una tabla de uso único que refleja todas las plantillas admitidas por el proveedor 
    
- Una tabla de uso único que refleja todas las plantillas que admiten todos los proveedores de la compatibilidad de perfiles, además de algunos que admite MAPI
    
Los proveedores que admiten los destinatarios de la creación implementan los dos primeros tipos, ya sea en un mensaje o en un contenedor. El proveedor puede incluir el mismo conjunto o un conjunto de plantillas diferente en las tablas de uso único. La diferencia principal entre los dos tipos radica en que la tabla de proveedor debe incluir plantillas para crear destinatarios que puedan usarse en mensajes salientes y la tabla de contenedores debe incluir plantillas para la creación de destinatarios que se van a agregar a su contenedor. Un contenedor solo puede admitir un conjunto restringido de plantillas, pero la tabla de un solo uso de proveedor debe incluir todas las plantillas admitidas por el proveedor.
  
MAPI implementa el tercer tipo de una tabla de uso único; los proveedores obtienen acceso a él llamando a [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md). La tabla de uso único de MAPI es la Unión de todas las tablas de proveedor; incluye todas las plantillas admitidas por cada proveedor en el perfil. También incluye plantillas compatibles con MAPI. El proveedor puede usar esta tabla en vez de la tabla solicitada para un contenedor. Sin embargo, las plantillas de esta tabla también pueden usarse para crear destinatarios para mensajes salientes.
  

