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
ms.openlocfilehash: 439927dc78941f086c025d77c76236497d3f4a15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425935"
---
# <a name="launching-a-form-to-read-a-message"></a>Iniciar un formulario para leer un mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los implementadores de servidores de formulario deben esperar la siguiente secuencia de llamadas de método a su servidor de formulario y objetos de formulario cuando una aplicación cliente carga un mensaje:
  
1. La aplicación cliente abre el administrador de formularios con una llamada a la [función MAPIOpenFormMgr.](mapiopenformmgr.md) 
    
2. La aplicación cliente llama al [método IMAPIFormMgr::LoadForm,](imapiformmgr-loadform.md) que devuelve un objeto [con IMAPIForm](imapiformiunknown.md). El administrador de formularios puede publicarse ahora si no se usará para otras activaciones de formularios. Tenga en cuenta que una llamada **a LoadForm** puede tardar algún tiempo porque es posible que el administrador de formularios tenga que instalar los archivos ejecutables del servidor de formularios antes de continuar. 
    
3. Opcionalmente, la aplicación cliente puede preparar [IMAPIViewContext](imapiviewcontextiunknown.md) para controlar las operaciones que pueden hacer que el objeto de formulario cargue el mensaje anterior o siguiente en la carpeta. La aplicación cliente puede usar el método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) para cambiar el contexto de vista predeterminado que se estableció en la **llamada LoadForm.** 
    
4. La aplicación cliente llama al [método IPersistMessage::Load](ipersistmessage-load.md) para cargar datos de mensajes en el objeto de formulario. 
    
5. La aplicación cliente llama a [IMAPIForm::D oVerb](imapiform-doverb.md) para invocar el verbo abierto, pasando el puntero opcional de la interfaz [IMAPIViewContext.](imapiviewcontextiunknown.md) 
    
## <a name="see-also"></a>Consulte también



[Interacciones del servidor de formulario](form-server-interactions.md)

