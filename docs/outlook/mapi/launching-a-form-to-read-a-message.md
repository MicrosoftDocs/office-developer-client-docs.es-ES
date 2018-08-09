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
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="096e9-103">Iniciar un formulario para leer un mensaje</span><span class="sxs-lookup"><span data-stu-id="096e9-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="096e9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="096e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="096e9-105">Los implementadores de servidor del formulario deben esperar la siguiente secuencia de llamadas de método a su servidor de formulario y los objetos de formulario cuando un mensaje carga una aplicación cliente:</span><span class="sxs-lookup"><span data-stu-id="096e9-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="096e9-106">La aplicación cliente, abre el Administrador de formulario con una llamada a la función [MAPIOpenFormMgr](mapiopenformmgr.md) .</span><span class="sxs-lookup"><span data-stu-id="096e9-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="096e9-107">La aplicación cliente llama al método [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) , que devuelve un objeto con [IMAPIForm](imapiformiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="096e9-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="096e9-108">El Administrador de formularios puede liberarse ahora si no se usará para aún más las activaciones de formulario.</span><span class="sxs-lookup"><span data-stu-id="096e9-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="096e9-109">Tenga en cuenta que una llamada a **LoadForm** puede tardar un poco debido a que el Administrador de formulario que tenga que instalar archivos ejecutables del servidor de formulario antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="096e9-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="096e9-110">De forma opcional, la aplicación cliente puede preparar [IMAPIViewContext](imapiviewcontextiunknown.md) para controlar las operaciones que pueden hacer que el objeto de formulario para cargar el mensaje anterior o siguiente en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="096e9-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="096e9-111">La aplicación cliente puede usar el método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) para cambiar el contexto de vista predeterminada que se estableció en la llamada **LoadForm** .</span><span class="sxs-lookup"><span data-stu-id="096e9-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="096e9-112">La aplicación cliente llama al método de [IPersistMessage::Load](ipersistmessage-load.md) para cargar los datos del mensaje en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="096e9-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="096e9-113">La aplicación cliente llama a [IMAPIForm::DoVerb](imapiform-doverb.md) para invocar el verbo open, pasando el puntero de interfaz [IMAPIViewContext](imapiviewcontextiunknown.md) opcional.</span><span class="sxs-lookup"><span data-stu-id="096e9-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="096e9-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="096e9-114">See also</span></span>



[<span data-ttu-id="096e9-115">Interacciones del servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="096e9-115">Form Server Interactions</span></span>](form-server-interactions.md)

