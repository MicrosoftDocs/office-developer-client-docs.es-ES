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
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="56189-103">Inicio de un nuevo formulario de redacción</span><span class="sxs-lookup"><span data-stu-id="56189-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="56189-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56189-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56189-105">Los implementadores del servidor de formularios deberían esperar la siguiente secuencia de llamadas a métodos a sus objetos de formulario y servidor de formularios cuando una aplicación cliente abre un nuevo mensaje para redacción:</span><span class="sxs-lookup"><span data-stu-id="56189-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="56189-106">La aplicación cliente llama al método [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para obtener información de clase sobre la clase de mensaje del servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="56189-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="56189-107">La aplicación cliente llama a [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) para obtener un nuevo objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="56189-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="56189-108">El administrador de formularios MAPI carga el servidor de formularios, si aún no está en la memoria, y obtiene una interfaz [IMAPIForm](imapiformiunknown.md) del servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="56189-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="56189-109">La aplicación cliente toma la interfaz **IMAPIForm** resultante y llama al método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) para obtener la interfaz [IPersistMessage](ipersistmessageiunknown.md) del objeto.</span><span class="sxs-lookup"><span data-stu-id="56189-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="56189-110">La aplicación cliente llama al método [IPersistMessage:: InitNew](ipersistmessage-initnew.md) para asociar el objeto Form a los objetos de [IMessage](imessageimapiprop.md), contexto de vista y receptor de aviso.</span><span class="sxs-lookup"><span data-stu-id="56189-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="56189-111">La aplicación cliente llama al método [IMAPIForm::D overb](imapiform-doverb.md) para invocar el verbo abierto.</span><span class="sxs-lookup"><span data-stu-id="56189-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="56189-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="56189-112">See also</span></span>



[<span data-ttu-id="56189-113">InterAcciones del servidor de formularios</span><span class="sxs-lookup"><span data-stu-id="56189-113">Form Server Interactions</span></span>](form-server-interactions.md)

