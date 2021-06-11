---
title: Iniciar un servidor de formularios
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
# <a name="launching-a-form-server"></a>Iniciar un servidor de formularios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La serie de interacciones que se producen cuando se carga un formulario desde el almacenamiento persistente (es decir, desde una biblioteca de formularios) para mostrar un mensaje es la siguiente:
  
1. El cliente de mensajería obtiene la clase de mensaje del mensaje, las marcas de mensaje y el estado del mensaje. Este paso es opcional; si estos datos no se proporcionan en el paso 2, el administrador de formularios los recuperará.
    
2. El cliente de mensajería llama [a IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) con el mensaje de destino. 
    
3. El administrador de formularios carga el servidor de formularios de la biblioteca de formularios adecuada. Si el servidor de formularios del mensaje de destino no está instalado, el administrador de formularios también instalará los archivos ejecutables del formulario.
    
4. El administrador de formularios llama a [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) en el objeto de formulario para obtener la IMAPIForm del objeto de formulario [: IUnknown](imapiformiunknown.md) e [IPersistMessage : interfaces IUnknown.](ipersistmessageiunknown.md) 
    
5. El administrador de formularios llama [a IPersistMessage::Load](ipersistmessage-load.md) con el sitio del mensaje y las interfaces de mensaje desde el objeto viewer. 
    
6. El objeto form vuelve a llamar al método [IMAPIMessageSite::GetSiteStatus del](imapimessagesite-getsitestatus.md) cliente de mensajería. 
    
7. El administrador de formularios llama al método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) del objeto de formulario con la interfaz de contexto de vista desde el cliente de mensajería. 
    
8. El objeto form vuelve a llamar al método [IMAPIViewContext::SetAdviseSink del](imapiviewcontext-setadvisesink.md) cliente de mensajería. 
    
9. El objeto form vuelve a llamar al método [IMAPIViewContext::GetViewStatus del](imapiviewcontext-getviewstatus.md) cliente de mensajería. 
    
10. El cliente de mensajería llama al método [IMAPIForm::Advise](imapiform-advise.md) del objeto de formulario con las interfaces de contexto de vista desde el objeto visor y el objeto de sitio del mensaje. 
    
11. El cliente de mensajería llama al método [IMAPIForm::D oVerb del](imapiform-doverb.md) objeto de formulario. 
    
12. El objeto form crea su interfaz de usuario, si es necesario, e interactúa con el usuario.
    
## <a name="see-also"></a>Vea también



[Interacciones del servidor de formulario](form-server-interactions.md)

