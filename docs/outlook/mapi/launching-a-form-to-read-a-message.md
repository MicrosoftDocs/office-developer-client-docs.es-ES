---
title: Iniciar un formulario para leer un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 675de7eeda534d8761887cdcb6d5c94a209ca18b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818026"
---
# <a name="launching-a-form-to-read-a-message"></a>Iniciar un formulario para leer un mensaje

  
  
**Hace referencia a**: Outlook 
  
Los implementadores de servidor del formulario deben esperar la siguiente secuencia de llamadas de método a su servidor de formulario y los objetos de formulario cuando un mensaje carga una aplicación cliente:
  
1. La aplicación cliente, abre el Administrador de formulario con una llamada a la función [MAPIOpenFormMgr](mapiopenformmgr.md) . 
    
2. La aplicación cliente llama al método [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) , que devuelve un objeto con [IMAPIForm](imapiformiunknown.md). El Administrador de formularios puede liberarse ahora si no se usará para aún más las activaciones de formulario. Tenga en cuenta que una llamada a **LoadForm** puede tardar un poco debido a que el Administrador de formulario que tenga que instalar archivos ejecutables del servidor de formulario antes de continuar. 
    
3. De forma opcional, la aplicación cliente puede preparar [IMAPIViewContext](imapiviewcontextiunknown.md) para controlar las operaciones que pueden hacer que el objeto de formulario para cargar el mensaje anterior o siguiente en la carpeta. La aplicación cliente puede usar el método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) para cambiar el contexto de vista predeterminada que se estableció en la llamada **LoadForm** . 
    
4. La aplicación cliente llama al método de [IPersistMessage::Load](ipersistmessage-load.md) para cargar los datos del mensaje en el objeto de formulario. 
    
5. La aplicación cliente llama a [IMAPIForm::DoVerb](imapiform-doverb.md) para invocar el verbo open, pasando el puntero de interfaz [IMAPIViewContext](imapiviewcontextiunknown.md) opcional. 
    
## <a name="see-also"></a>Vea también



[Interacciones del servidor de formulario](form-server-interactions.md)

