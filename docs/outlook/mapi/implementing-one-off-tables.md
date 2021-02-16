---
title: Implementación de One-Off tablas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c29feae84d81874988997409fd229b042a701640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421644"
---
# <a name="implementing-one-off-tables"></a>Implementación de One-Off tablas

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El proveedor puede implementar una o varias tablas de aplicación única. Una tabla de uso único es una lista resumida de plantillas de uso único que se usan para crear destinatarios, ya sea directamente en un contenedor o en la lista de destinatarios de un mensaje saliente. Una plantilla de uso único es un formulario que los usuarios emplean para escribir datos relevantes para un tipo determinado de dirección. Cuando el usuario termina de trabajar con la plantilla, el proveedor crea el nuevo destinatario y lo agrega al mensaje. Normalmente, cada plantilla controla un único tipo de dirección. Sin embargo, es posible que una plantilla controle varios tipos o que varias plantillas controle el mismo tipo. 
  
El proveedor debe admitir el **método OpenEntry** para cada plantilla que incluya en la tabla de uso único. La implementación de **OpenEntry debe** recuperar una tabla para mostrar para la plantilla. MAPI usa la tabla para mostrar para que la plantilla sea visible para el usuario. 
  
Aunque la mayoría de las filas de las tablas de uso único representan plantillas, algunas de las filas se pueden usar para clasificar o agrupar plantillas. El valor de su columna PR_SELECTABLE **(** [PidTagSelectable](pidtagselectable-canonical-property.md)) indica si una fila de una tabla de uso único representa o no una plantilla. Las filas que representan plantillas tienen la PR_SELECTABLE establecida en TRUE; las filas que no representan plantillas tienen el valor FALSE.
  
MAPI define tres tipos de tablas de uso único:
  
- Una tabla de uso único que refleja las plantillas que admite un contenedor individual
    
- Una tabla de uso único que refleja todas las plantillas compatibles con el proveedor 
    
- Una tabla de uso único que refleja todas las plantillas que admiten todos los proveedores del perfil, además de algunas compatibles con MAPI
    
Los dos primeros tipos los implementan los proveedores que admiten los destinatarios de creación, ya sea en un mensaje o en un contenedor. El proveedor puede incluir el mismo conjunto o un conjunto de plantillas diferente en sus tablas de uso único. La principal diferencia entre los dos tipos es que la tabla del proveedor debe incluir plantillas para crear destinatarios que se puedan usar en los mensajes salientes y la tabla contenedora debe incluir plantillas para crear destinatarios que se agregarán al contenedor. Un contenedor solo puede admitir un conjunto restringido de plantillas, pero la tabla de uso único del proveedor debe incluir todas las plantillas que admite el proveedor.
  
MAPI implementa el tercer tipo de tabla de uso único; los proveedores obtienen acceso a él llamando a [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). La tabla de uso único mapi es la unión de todas las tablas de proveedor; incluye todas las plantillas admitidas por todos los proveedores del perfil. También incluye plantillas compatibles con MAPI. El proveedor puede usar esta tabla en lugar de la tabla solicitada para un contenedor. Sin embargo, las plantillas de esta tabla también se pueden usar para crear destinatarios para los mensajes salientes.
  

