---
title: Iniciar un servidor de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: dec8706ba00356660ec82c25e0213ef3e638691d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387730"
---
# <a name="launching-a-form-server"></a>Iniciar un servidor de formulario

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
La serie de interacciones que se produce cuando se carga un formulario desde el almacenamiento persistente (es decir, desde una biblioteca de formularios) mostrar un mensaje es como sigue:
  
1. El cliente de mensajería Obtiene la clase de mensaje del mensaje, indicadores de mensaje y estado del mensaje. Este paso es opcional; Si no se proporcionan estos fragmentos de datos en el paso 2, el Administrador de formularios, recuperará ellos.
    
2. El cliente de mensajería llama a [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) con el mensaje de destino. 
    
3. El Administrador de formularios de carga el servidor de formulario desde la biblioteca de forma adecuada. Si no está instalado el servidor de formulario para el mensaje de destino, el Administrador de formulario instala los archivos del formulario ejecutable, así como.
    
4. El Administrador de formulario llama a [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) en el objeto de formulario para obtener el objeto de formulario [IMAPIForm: IUnknown](imapiformiunknown.md) y [IPersistMessage: IUnknown](ipersistmessageiunknown.md) interfaces. 
    
5. El Administrador de formulario llama a [IPersistMessage::Load](ipersistmessage-load.md) con el mensaje de interfaces de sitio y de mensaje del objeto Visor. 
    
6. El objeto de formulario vuelve a llamar al método de [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) del cliente de mensajería. 
    
7. El Administrador de formulario llama el formulario método del objeto [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) con la interfaz de contexto de vista desde el cliente de mensajería. 
    
8. El objeto de formulario vuelve a llamar al método de [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) del cliente de mensajería. 
    
9. El objeto de formulario vuelve a llamar al método de [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) del cliente de mensajería. 
    
10. El cliente de mensajería llama el formulario método del objeto [IMAPIForm::Advise](imapiform-advise.md) con la vista de interfaces de contexto desde el objeto Visor y el objeto de sitio de mensaje. 
    
11. El cliente de mensajería llama el formulario método del objeto [IMAPIForm::DoVerb](imapiform-doverb.md) . 
    
12. El objeto de formulario crea su interfaz de usuario, si es necesario e interactúa con el usuario.
    
## <a name="see-also"></a>Vea también



[Interacciones del servidor de formulario](form-server-interactions.md)

