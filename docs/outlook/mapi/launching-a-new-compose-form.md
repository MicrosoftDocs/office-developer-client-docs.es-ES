---
title: Iniciar un nuevo formulario de redacción
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 29d53ba1242014a501a01d161c19dade164f393a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391776"
---
# <a name="launching-a-new-compose-form"></a>Iniciar un nuevo formulario de redacción

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Los implementadores de servidor del formulario deben esperar la siguiente secuencia de llamadas a métodos a su servidor de formulario y objetos de formulario cuando una aplicación cliente abre un nuevo mensaje para redactar:
  
1. La aplicación cliente llama al método de [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para obtener información de clase acerca de la clase de mensaje del servidor de formulario. 
    
2. La aplicación cliente llama a [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) para obtener un nuevo objeto de formulario. 
    
3. El Administrador de formularios MAPI carga el servidor de formulario, si aún no está en la memoria y obtiene una interfaz [IMAPIForm](imapiformiunknown.md) desde el servidor de formulario. 
    
4. La aplicación cliente toma la interfaz **IMAPIForm** resultante y llama al método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) para obtener la interfaz del objeto [IPersistMessage](ipersistmessageiunknown.md) . 
    
5. La aplicación cliente llama al método de [IPersistMessage::InitNew](ipersistmessage-initnew.md) para asociar el objeto de formulario con [IMessage](imessageimapiprop.md), contexto de vista y objetos del receptor de aviso.
    
6. La aplicación cliente llama al método de [IMAPIForm::DoVerb](imapiform-doverb.md) para invocar el verbo abrir. 
    
## <a name="see-also"></a>Vea también



[Interacciones del servidor de formulario](form-server-interactions.md)

