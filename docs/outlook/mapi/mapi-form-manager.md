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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351453"
---
# <a name="mapi-form-manager"></a>Administrador de formularios MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un administrador de formularios es un objeto que implementa la interfaz [IMAPIFormMgr](imapiformmgriunknown.md) . La mayoría de las organizaciones usarán el administrador de formularios suministrado con MAPI, al que se conoce como el administrador de formularios predeterminado. Sin embargo, una organización puede reemplazar el administrador de formularios predeterminado con un administrador de formularios personalizado si lo desea. El administrador de formularios se ocupa de localizar los formularios en las bibliotecas de formularios, cargar los formularios en respuesta a las solicitudes de los usuarios e instalar formularios en la biblioteca de formularios local de un usuario, en la biblioteca de formularios de carpeta o en la biblioteca de formularios personales. 
  
Para que un usuario interactúe con un mensaje, debe crearse una instancia del servidor de formularios para la clase de mensaje del mensaje y activarse para mostrar el mensaje y llevar a cabo la operación solicitada en el mensaje. Como se describe en el tema [bibliotecas de formularios MAPI](mapi-form-libraries.md), la implementación de un formulario puede existir en varias ubicaciones (bibliotecas de formularios) y no hay ninguna garantía de que un formulario o su servidor vayan a estar localmente disponibles o en estado de ejecución cuando un usuario desee interactuar con ella. El administrador de formularios se ocupa de los detalles de ubicación y activación del formulario.
  
Los clientes usan servicios proporcionados por el administrador de formularios para buscar y activar formularios. La interfaz **IMAPIFormMgr** es implementada por el administrador de formularios y los clientes la llaman para tener acceso a sus servicios. El administrador de formularios es un componente esencial porque oculta casi todos los detalles de búsqueda y activación de formularios desde clientes de mensajería. 
  
Al cargar servidores de formularios, el administrador de formulario predeterminado carga el formulario desde la primera biblioteca de formularios en la que se encuentra una implementación de la clase de mensaje del formulario. El administrador de formularios predeterminado busca las bibliotecas de formularios en el siguiente orden:
  
1. La biblioteca de formularios local del usuario. Se busca primero en esta biblioteca de formularios porque proporciona el acceso más rápido a la implementación de un formulario si la implementación se instala en la biblioteca de formularios local.
    
2. La biblioteca de formularios de la carpeta del contenedor del mensaje: la carpeta en la que se almacena el mensaje que se está cargando.
    
3. La biblioteca de formularios personal del usuario.
    
Un administrador de formularios personalizado puede buscar en las bibliotecas de formularios disponibles en cualquier orden o puede implementar otras bibliotecas de formularios, por ejemplo, una biblioteca de formularios para toda la organización. Para obtener más información sobre las bibliotecas de formularios, consulte [bibliotecas de formularios MAPI](mapi-form-libraries.md). 
  
## <a name="see-also"></a>Vea también



[Formularios MAPI](mapi-forms.md)

