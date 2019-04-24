---
title: Inicio de un nuevo formulario de redacción
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 29d53ba1242014a501a01d161c19dade164f393a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270059"
---
# <a name="launching-a-new-compose-form"></a>Inicio de un nuevo formulario de redacción

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los implementadores del servidor de formularios deberían esperar la siguiente secuencia de llamadas a métodos a sus objetos de formulario y servidor de formularios cuando una aplicación cliente abre un nuevo mensaje para redacción:
  
1. La aplicación cliente llama al método [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para obtener información de clase sobre la clase de mensaje del servidor de formularios. 
    
2. La aplicación cliente llama a [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) para obtener un nuevo objeto de formulario. 
    
3. El administrador de formularios MAPI carga el servidor de formularios, si aún no está en la memoria, y obtiene una interfaz [IMAPIForm](imapiformiunknown.md) del servidor de formularios. 
    
4. La aplicación cliente toma la interfaz **IMAPIForm** resultante y llama al método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) para obtener la interfaz [IPersistMessage](ipersistmessageiunknown.md) del objeto. 
    
5. La aplicación cliente llama al método [IPersistMessage:: InitNew](ipersistmessage-initnew.md) para asociar el objeto Form a los objetos de [IMessage](imessageimapiprop.md), contexto de vista y receptor de aviso.
    
6. La aplicación cliente llama al método [IMAPIForm::D overb](imapiform-doverb.md) para invocar el verbo abierto. 
    
## <a name="see-also"></a>Vea también



[InterAcciones del servidor de formularios](form-server-interactions.md)

