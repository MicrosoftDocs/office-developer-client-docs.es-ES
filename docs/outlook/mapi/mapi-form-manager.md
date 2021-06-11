---
title: Administrador de formularios MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3059183103ca2552505486b5ec54366729ae4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430199"
---
# <a name="mapi-form-manager"></a>Administrador de formularios MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un administrador de formularios es un objeto que implementa la [interfaz IMAPIFormMgr.](imapiformmgriunknown.md) La mayoría de las organizaciones usarán el administrador de formularios proporcionado con MAPI, denominado administrador de formularios predeterminado. Sin embargo, una organización puede reemplazar el administrador de formularios predeterminado por un administrador de formularios personalizado si lo desea. El administrador de formularios se encarga de localizar formularios en bibliotecas de formularios, cargar formularios en respuesta a solicitudes de usuario e instalar formularios en la biblioteca de formularios local, biblioteca de formularios de carpetas o biblioteca de formularios personal de un usuario. 
  
Para que un usuario interactúe con un mensaje, se debe crear y activar una instancia del servidor de formulario para la clase de mensaje del mensaje para mostrar el mensaje y llevar a cabo la operación solicitada en el mensaje. Como se describe en el tema Bibliotecas de [formularios MAPI,](mapi-form-libraries.md)la implementación de un formulario puede existir en varias ubicaciones diferentes (bibliotecas de formularios) y no hay ninguna garantía de que un formulario o su servidor estarán disponibles localmente o en un estado en ejecución cuando un usuario quiera interactuar con él. El administrador de formularios se encarga de los detalles de la localización y activación del formulario.
  
Los clientes usan los servicios proporcionados por el administrador de formularios para buscar y activar formularios. El administrador de formularios implementa la interfaz **IMAPIFormMgr** y los clientes los llaman para obtener acceso a sus servicios. El administrador de formularios es un componente esencial porque oculta casi todos los detalles de la búsqueda y activación de formularios de clientes de mensajería. 
  
Al cargar servidores de formulario, el administrador de formularios predeterminado carga el formulario desde la primera biblioteca de formularios en la que se encuentra una implementación para la clase de mensaje del formulario. El administrador de formularios predeterminado busca en las bibliotecas de formularios en el orden siguiente:
  
1. Biblioteca de formularios local del usuario. Esta biblioteca de formularios se busca primero porque proporciona el acceso más rápido a la implementación de un formulario si la implementación está instalada en la biblioteca de formularios local.
    
2. La biblioteca de formularios de carpeta del contenedor del mensaje: la carpeta en la que se almacena el mensaje que se está cargando.
    
3. Biblioteca de formularios personal del usuario.
    
Un administrador de formularios personalizado puede buscar en las bibliotecas de formularios disponibles en cualquier orden o puede implementar otras bibliotecas de formularios, como una biblioteca de formularios de toda la organización. Para obtener más información sobre bibliotecas de formularios, vea [Bibliotecas de formularios MAPI](mapi-form-libraries.md). 
  
## <a name="see-also"></a>Vea también



[Formularios MAPI](mapi-forms.md)

