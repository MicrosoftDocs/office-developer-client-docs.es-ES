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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333022"
---
# <a name="creating-a-form-configuration-file"></a>Creación de un archivo de configuración de formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un archivo de configuración de formulario proporciona información sobre un formulario tanto al administrador de formularios que se utiliza como a las aplicaciones cliente. Un archivo de configuración de formulario contiene una completa especificación para un formulario, incluidas las propiedades publicadas por el formulario para que las usen los clientes de mensajería, los verbos implementados por el formulario y las plataformas admitidas por el formulario.
  
Un archivo de configuración de formulario es un archivo con una extensión. cfg y tiene un formato similar a un archivo de inicialización de Windows. Se trata de un archivo de texto sin formato con una serie de secciones. Cada sección comienza con un nombre de sección, entre corchetes. Cada sección contiene una o varias líneas que definen los valores y la configuración relevantes para dicha sección. Los valores tienen uno de los siguientes tipos:
  
- String
    
- Cadena mostrada
    
- Cadena de la plataforma
    
- Nombre de ruta de acceso
    
- Entero
    
- GUID
    
Para obtener más información acerca de las secciones de un archivo. cfg, vea el [formato de archivo de los archivos de configuración de formulario](file-format-of-form-configuration-files.md).
  
## <a name="see-also"></a>Vea también



[Desarrollar servidores de formulario MAPI](developing-mapi-form-servers.md)

