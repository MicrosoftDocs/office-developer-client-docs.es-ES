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
# <a name="launching-a-form-server"></a><span data-ttu-id="4a9c9-103">Iniciar un servidor de formularios</span><span class="sxs-lookup"><span data-stu-id="4a9c9-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="4a9c9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a9c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a9c9-105">La serie de interacciones que se producen cuando se carga un formulario desde el almacenamiento persistente (es decir, desde una biblioteca de formularios) para mostrar un mensaje es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="4a9c9-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="4a9c9-106">El cliente de mensajería obtiene la clase de mensaje del mensaje, las marcas de mensaje y el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="4a9c9-107">Este paso es opcional; si estos datos no se proporcionan en el paso 2, el administrador de formularios los recuperará.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="4a9c9-108">El cliente de mensajería llama [a IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) con el mensaje de destino.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="4a9c9-109">El administrador de formularios carga el servidor de formularios de la biblioteca de formularios adecuada.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="4a9c9-110">Si el servidor de formularios del mensaje de destino no está instalado, el administrador de formularios también instalará los archivos ejecutables del formulario.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="4a9c9-111">El administrador de formularios llama a [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) en el objeto de formulario para obtener la IMAPIForm del objeto de formulario [: IUnknown](imapiformiunknown.md) e [IPersistMessage : interfaces IUnknown.](ipersistmessageiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="4a9c9-111">The form manager calls [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="4a9c9-112">El administrador de formularios llama [a IPersistMessage::Load](ipersistmessage-load.md) con el sitio del mensaje y las interfaces de mensaje desde el objeto viewer.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="4a9c9-113">El objeto form vuelve a llamar al método [IMAPIMessageSite::GetSiteStatus del](imapimessagesite-getsitestatus.md) cliente de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="4a9c9-114">El administrador de formularios llama al método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) del objeto de formulario con la interfaz de contexto de vista desde el cliente de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="4a9c9-115">El objeto form vuelve a llamar al método [IMAPIViewContext::SetAdviseSink del](imapiviewcontext-setadvisesink.md) cliente de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="4a9c9-116">El objeto form vuelve a llamar al método [IMAPIViewContext::GetViewStatus del](imapiviewcontext-getviewstatus.md) cliente de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="4a9c9-117">El cliente de mensajería llama al método [IMAPIForm::Advise](imapiform-advise.md) del objeto de formulario con las interfaces de contexto de vista desde el objeto visor y el objeto de sitio del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="4a9c9-118">El cliente de mensajería llama al método [IMAPIForm::D oVerb del](imapiform-doverb.md) objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="4a9c9-119">El objeto form crea su interfaz de usuario, si es necesario, e interactúa con el usuario.</span><span class="sxs-lookup"><span data-stu-id="4a9c9-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a9c9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a9c9-120">See also</span></span>



[<span data-ttu-id="4a9c9-121">Interacciones del servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="4a9c9-121">Form Server Interactions</span></span>](form-server-interactions.md)

