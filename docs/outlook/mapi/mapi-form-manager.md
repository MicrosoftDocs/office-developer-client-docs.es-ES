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
ms.openlocfilehash: f78c25285c7ac3f8736006e4a45079a7d9a6d867
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592300"
---
# <a name="mapi-form-manager"></a>Administrador de formularios MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El Administrador de un formulario es un objeto que implementa la interfaz [IMAPIFormMgr](imapiformmgriunknown.md) . La mayoría de las organizaciones utilizará el Administrador de formulario que se proporciona con MAPI, que se conoce como el Administrador de forma predeterminada. Sin embargo, una organización puede reemplazar el Administrador de formulario predeterminado con el Administrador de un formulario personalizado, si así lo desea. El Administrador de formulario se encarga de localizar formularios dentro de las bibliotecas de formularios, carga de los formularios en respuesta a las solicitudes de usuario e instalar formularios en la biblioteca de formularios local, biblioteca de formularios de carpeta o biblioteca de formularios personales de un usuario. 
  
Para un usuario interactuar con un mensaje, una instancia del servidor de formulario para la clase de mensaje del mensaje debe ser creada y activada para mostrar el mensaje y realizar la operación solicitada en el mensaje. Tal como se describe en el tema de [Las bibliotecas de formularios de MAPI](mapi-form-libraries.md), la implementación de un formulario puede existir en varias ubicaciones diferentes (bibliotecas de formularios) y no hay ninguna garantía de que un formulario o en su servidor va a estar disponible localmente o en una ejecución de estado cuando un usuario desea interactuar con él. El Administrador de formulario se encarga de los detalles de localizar y activar el formulario.
  
Los clientes usan los servicios proporcionados por el Administrador de formularios para encontrar y activar formularios. La interfaz de **IMAPIFormMgr** se implementa mediante el Administrador de formulario y se llama por los clientes para tener acceso a sus servicios. El Administrador de formulario es un componente esencial porque oculta casi todos los detalles de búsqueda y activación de los formularios de clientes de mensajería. 
  
Al cargar los servidores de formulario, el Administrador de formulario predeterminado carga el formulario desde la primera biblioteca de formularios en la que se encuentra una implementación para la clase de mensaje del formulario. El Administrador de formulario predeterminado busca las bibliotecas de formularios en el orden siguiente:
  
1. Biblioteca de formulario local del usuario. Esta biblioteca de formularios se busca en primer lugar porque proporciona el acceso más rápido a la implementación de un formulario si la implementación está instalada en la biblioteca de formularios local.
    
2. La biblioteca de formularios de la carpeta de contenedor del mensaje: la carpeta en la que está almacenado el mensaje que se está cargando.
    
3. Biblioteca de formularios personal del usuario.
    
El Administrador de un formulario personalizado puede buscar las bibliotecas de formulario disponibles en cualquier orden, o puede implementar otras bibliotecas de formularios, como una biblioteca de formularios de toda la organización. Para obtener más detalles sobre las bibliotecas de formularios, vea [Bibliotecas de formularios de MAPI](mapi-form-libraries.md). 
  
## <a name="see-also"></a>Recursos adicionales



[Formularios MAPI](mapi-forms.md)

