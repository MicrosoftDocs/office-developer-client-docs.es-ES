---
title: Creación de un archivo de configuración de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425221"
---
# <a name="creating-a-form-configuration-file"></a>Creación de un archivo de configuración de formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un archivo de configuración de formulario proporciona información sobre un formulario tanto para el administrador de formularios que se usa como para las aplicaciones cliente. Un archivo de configuración de formulario contiene una amplia especificación para un formulario, incluidas las propiedades publicadas por el formulario para su uso por los clientes de mensajería, los verbos implementados por el formulario y las plataformas admitidas por el formulario.
  
Un archivo de configuración de formulario es un archivo con una extensión .cfg y tiene un formato similar a un Windows de inicialización. Es un archivo de texto sin formato con varias secciones. Cada sección comienza con un nombre de sección, entre corchetes. Cada sección contiene una o más líneas que definen valores y configuraciones relevantes para esa sección. Los valores tienen uno de los siguientes tipos:
  
- Cadena
    
- Cadena mostrada
    
- Cadena de plataforma
    
- Nombre de ruta de acceso
    
- Entero
    
- GUID
    
Para obtener más información acerca de las secciones de un archivo .cfg, vea [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).
  
## <a name="see-also"></a>Vea también



[Desarrollo de servidores de formulario MAPI](developing-mapi-form-servers.md)

