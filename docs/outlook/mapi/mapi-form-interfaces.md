---
title: Interfaces de formulario de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412348"
---
# <a name="mapi-form-interfaces"></a>Interfaces de formulario de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI define las siguientes interfaces relacionadas con los formularios.
  
|**Nombre de interfaz**|**Descripción**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |Manipula los objetos de formulario y controla los comandos de objeto de formulario.  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |Determina si el objeto de formulario puede controlar el siguiente mensaje y cambia el estado siguiente o anterior del objeto de formulario.  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |Admite la instalación, desinstalación y resolución de servidores de formularios en un contenedor de formularios específico.  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |Admite el uso de servidores de formulario en tiempo de ejecución configurables.  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |Permite a las aplicaciones cliente trabajar con propiedades específicas de una clase de mensaje.  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |Permite a las aplicaciones cliente obtener información acerca de los servidores de formularios, activar servidores de formularios e instalar servidores de formularios en el sistema de mensajería.  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |Se usa para manipular los mensajes asociados con objetos de formulario.  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |Notifica a las aplicaciones cliente que se ha producido un evento en el objeto Form.  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |Se usa para responder a los comandos siguiente, anterior y eliminar en el objeto de formulario.  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |Se usa para guardar, inicializar y cargar objetos de formulario en el almacenamiento de mensajes.  <br/> |
   
Para obtener más información acerca de los métodos de las interfaces de formulario de MAPI, vea la documentación de estas interfaces. No es necesario implementar todas las interfaces de formulario MAPI para crear un formulario personalizado. Un formulario solo requiere que se implementen las interfaces **IPersistMessage**, **IMAPIForm**y **IMAPIFormAdviseSink** . Además, también es una buena idea implementar **IMAPIFormFactory** y **IMAPIFormInfo**. **IMAPIFormFactory** es útil para el cumplimiento de OLE, y **IMAPIFormInfo** permite que las aplicaciones de cliente bien escritas usen mejor los formularios. 
  
> [!NOTE]
> Hablando estrictamente, **IMAPIFormAdviseSink** es una interfaz opcional. Sin embargo, se recomienda encarecidamente implementarlo en los servidores de formularios. Esta interfaz es fundamental para la interacción eficaz entre los clientes de mensajería y los servidores de formularios, sobre todo cuando se trata de varios mensajes de la clase de mensaje de su servidor de formularios. 
  
## <a name="see-also"></a>Ver también



[Formularios MAPI](mapi-forms.md)

