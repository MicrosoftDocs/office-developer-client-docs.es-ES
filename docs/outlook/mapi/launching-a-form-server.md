---
title: Inicio de un servidor de formularios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: dec8706ba00356660ec82c25e0213ef3e638691d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270052"
---
# <a name="launching-a-form-server"></a>Inicio de un servidor de formularios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La serie de interacciones que se produce cuando se carga un formulario desde un almacenamiento persistente (es decir, desde una biblioteca de formularios) para mostrar un mensaje es la siguiente:
  
1. El cliente de mensajería obtiene la clase de mensaje, las marcas de mensaje y el estado del mensaje del mensaje. Este paso es opcional; Si estos fragmentos de datos no se proporcionan en el paso 2, el administrador de formularios los recuperará.
    
2. El cliente de mensajería llama a [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) con el mensaje de destino. 
    
3. El administrador de formularios carga el servidor de formularios desde la biblioteca de formularios correspondiente. Si el servidor de formularios para el mensaje de destino no está instalado, el administrador de formularios instala también los archivos ejecutables del formulario.
    
4. El administrador de formularios llama a [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) en el objeto de formulario para obtener las interfaces [IMAPIForm: IUnknown](imapiformiunknown.md) y [IPersistMessage: IUnknown](ipersistmessageiunknown.md) del objeto Form. 
    
5. El administrador de formularios llama a [IPersistMessage:: Load](ipersistmessage-load.md) con el sitio de mensajes y las interfaces de mensajes del objeto Viewer. 
    
6. El objeto de formulario vuelve a llamar al método [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md) del cliente de mensajería. 
    
7. El administrador de formularios llama al método [IMAPIForm:: SetViewContext](imapiform-setviewcontext.md) del objeto Form con la interfaz de contexto de vista del cliente de mensajería. 
    
8. El objeto de formulario vuelve a llamar al método [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) del cliente de mensajería. 
    
9. El objeto de formulario vuelve a llamar al método [IMAPIViewContext:: GetViewStatus](imapiviewcontext-getviewstatus.md) del cliente de mensajería. 
    
10. El cliente de mensajería llama al método [IMAPIForm:: Advise](imapiform-advise.md) del objeto Form con las interfaces de contexto de vista del objeto de visor y del objeto de sitio de mensaje. 
    
11. El cliente de mensajería llama al método [IMAPIForm::D overb](imapiform-doverb.md) del objeto Form. 
    
12. El objeto Form crea su interfaz de usuario, si es necesario, e interactúa con el usuario.
    
## <a name="see-also"></a>Vea también



[InterAcciones del servidor de formularios](form-server-interactions.md)

