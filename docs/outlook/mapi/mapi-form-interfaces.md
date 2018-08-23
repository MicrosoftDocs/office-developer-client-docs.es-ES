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
ms.openlocfilehash: f37d398167e8210a2fd67ff08e63572eb6c9db9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585727"
---
# <a name="mapi-form-interfaces"></a>Interfaces de formulario de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI define las interfaces siguientes relativas a los formularios.
  
|**Nombre de la interfaz**|**Descripción**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |Manipula los objetos formulario y administra los comandos de objeto de formulario.  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |Determina si el objeto de formulario, puede controlar el siguiente mensaje y cambia el estado siguiente o anterior del objeto de formulario.  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |Es compatible con la instalación, desinstalación y solución de servidores de formulario frente a un contenedor de forma específicos.  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |Admite el uso de servidores de formulario configurable de tiempo de ejecución.  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |Permite a las aplicaciones de cliente trabajar con las propiedades que son específicas de una clase de mensaje.  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |Permite a las aplicaciones de cliente obtener información acerca de los servidores de formulario, activa los servidores de formulario y servidores de formulario se instala en el sistema de mensajería.  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |Se usa para manipular los mensajes asociados a objetos de formulario.  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |Notifica a las aplicaciones de cliente que se ha producido un evento en el objeto de formulario.  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |Se usa para responder a la siguiente, anterior y eliminar comandos en el objeto de formulario.  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |Se usa para guardar, inicializar y cargar los objetos de formulario a y desde el almacenamiento de mensajes.  <br/> |
   
Para obtener más información acerca de los métodos de las interfaces de formulario MAPI, consulte la documentación para estas interfaces. No es necesario implementar todas las interfaces de formulario MAPI para crear un formulario personalizado. Un formulario propio sólo requiere que implementar el **IPersistMessage**, **IMAPIForm**, y **IMAPIFormAdviseSink** interfaces. Además, también es una buena idea para implementar **IMAPIFormFactory** y **IMAPIFormInfo**. **IMAPIFormFactory** es útil para el cumplimiento de OLE y **IMAPIFormInfo** permite a las aplicaciones cliente bien escrito hacer un mejor uso de los formularios. 
  
> [!NOTE]
> En realidad, **IMAPIFormAdviseSink** es una interfaz opcional. Sin embargo, se recomienda encarecidamente que se implemente en los servidores de formulario. Esta interfaz es fundamental para la interacción eficaz entre clientes de mensajería y los servidores de formulario, especialmente cuando varios mensajes de su servidor de formulario clase de mensaje que se trate. 
  
## <a name="see-also"></a>Recursos adicionales



[Formularios MAPI](mapi-forms.md)

