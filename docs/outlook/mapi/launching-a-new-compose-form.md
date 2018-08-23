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
ms.openlocfilehash: 66aa5fe08b1c0be3906fa9a0483bbdec37c095c5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564503"
---
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="30bfa-103">Iniciar un nuevo formulario de redacción</span><span class="sxs-lookup"><span data-stu-id="30bfa-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="30bfa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30bfa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30bfa-105">Los implementadores de servidor del formulario deben esperar la siguiente secuencia de llamadas a métodos a su servidor de formulario y objetos de formulario cuando una aplicación cliente abre un nuevo mensaje para redactar:</span><span class="sxs-lookup"><span data-stu-id="30bfa-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="30bfa-106">La aplicación cliente llama al método de [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para obtener información de clase acerca de la clase de mensaje del servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="30bfa-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="30bfa-107">La aplicación cliente llama a [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) para obtener un nuevo objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="30bfa-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="30bfa-108">El Administrador de formularios MAPI carga el servidor de formulario, si aún no está en la memoria y obtiene una interfaz [IMAPIForm](imapiformiunknown.md) desde el servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="30bfa-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="30bfa-109">La aplicación cliente toma la interfaz **IMAPIForm** resultante y llama al método [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) para obtener la interfaz del objeto [IPersistMessage](ipersistmessageiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="30bfa-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="30bfa-110">La aplicación cliente llama al método de [IPersistMessage::InitNew](ipersistmessage-initnew.md) para asociar el objeto de formulario con [IMessage](imessageimapiprop.md), contexto de vista y objetos del receptor de aviso.</span><span class="sxs-lookup"><span data-stu-id="30bfa-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="30bfa-111">La aplicación cliente llama al método de [IMAPIForm::DoVerb](imapiform-doverb.md) para invocar el verbo abrir.</span><span class="sxs-lookup"><span data-stu-id="30bfa-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="30bfa-112">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="30bfa-112">See also</span></span>



[<span data-ttu-id="30bfa-113">Interacciones del servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="30bfa-113">Form Server Interactions</span></span>](form-server-interactions.md)

