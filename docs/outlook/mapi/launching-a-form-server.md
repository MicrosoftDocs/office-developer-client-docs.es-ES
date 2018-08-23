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
ms.openlocfilehash: 87299ce4335492a744dd4ee965b4f8b85bcedc84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564895"
---
# <a name="launching-a-form-server"></a><span data-ttu-id="32c47-103">Iniciar un servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="32c47-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="32c47-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32c47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32c47-105">La serie de interacciones que se produce cuando se carga un formulario desde el almacenamiento persistente (es decir, desde una biblioteca de formularios) mostrar un mensaje es como sigue:</span><span class="sxs-lookup"><span data-stu-id="32c47-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="32c47-106">El cliente de mensajería Obtiene la clase de mensaje del mensaje, indicadores de mensaje y estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="32c47-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="32c47-107">Este paso es opcional; Si no se proporcionan estos fragmentos de datos en el paso 2, el Administrador de formularios, recuperará ellos.</span><span class="sxs-lookup"><span data-stu-id="32c47-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="32c47-108">El cliente de mensajería llama a [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) con el mensaje de destino.</span><span class="sxs-lookup"><span data-stu-id="32c47-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="32c47-109">El Administrador de formularios de carga el servidor de formulario desde la biblioteca de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="32c47-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="32c47-110">Si no está instalado el servidor de formulario para el mensaje de destino, el Administrador de formulario instala los archivos del formulario ejecutable, así como.</span><span class="sxs-lookup"><span data-stu-id="32c47-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="32c47-111">El Administrador de formulario llama a [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) en el objeto de formulario para obtener el objeto de formulario [IMAPIForm: IUnknown](imapiformiunknown.md) y [IPersistMessage: IUnknown](ipersistmessageiunknown.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="32c47-111">The form manager calls [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="32c47-112">El Administrador de formulario llama a [IPersistMessage::Load](ipersistmessage-load.md) con el mensaje de interfaces de sitio y de mensaje del objeto Visor.</span><span class="sxs-lookup"><span data-stu-id="32c47-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="32c47-113">El objeto de formulario vuelve a llamar al método de [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) del cliente de mensajería.</span><span class="sxs-lookup"><span data-stu-id="32c47-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="32c47-114">El Administrador de formulario llama el formulario método del objeto [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) con la interfaz de contexto de vista desde el cliente de mensajería.</span><span class="sxs-lookup"><span data-stu-id="32c47-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="32c47-115">El objeto de formulario vuelve a llamar al método de [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) del cliente de mensajería.</span><span class="sxs-lookup"><span data-stu-id="32c47-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="32c47-116">El objeto de formulario vuelve a llamar al método de [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) del cliente de mensajería.</span><span class="sxs-lookup"><span data-stu-id="32c47-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="32c47-117">El cliente de mensajería llama el formulario método del objeto [IMAPIForm::Advise](imapiform-advise.md) con la vista de interfaces de contexto desde el objeto Visor y el objeto de sitio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="32c47-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="32c47-118">El cliente de mensajería llama el formulario método del objeto [IMAPIForm::DoVerb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="32c47-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="32c47-119">El objeto de formulario crea su interfaz de usuario, si es necesario e interactúa con el usuario.</span><span class="sxs-lookup"><span data-stu-id="32c47-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32c47-120">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="32c47-120">See also</span></span>



[<span data-ttu-id="32c47-121">Interacciones del servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="32c47-121">Form Server Interactions</span></span>](form-server-interactions.md)

