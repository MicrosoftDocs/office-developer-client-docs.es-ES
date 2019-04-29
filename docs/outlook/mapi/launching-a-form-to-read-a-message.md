---
title: Inicio de un formulario para leer un mensaje
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
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="299be-103">Inicio de un formulario para leer un mensaje</span><span class="sxs-lookup"><span data-stu-id="299be-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="299be-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="299be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="299be-105">Los implementadores del servidor de formularios deberían esperar la siguiente secuencia de llamadas a métodos a sus objetos de formulario y servidor de formularios cuando una aplicación cliente carga un mensaje:</span><span class="sxs-lookup"><span data-stu-id="299be-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="299be-106">La aplicación cliente abre el administrador de formularios con una llamada a la función [MAPIOpenFormMgr](mapiopenformmgr.md) .</span><span class="sxs-lookup"><span data-stu-id="299be-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="299be-107">La aplicación cliente llama al método [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) , que devuelve un objeto con [IMAPIForm](imapiformiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="299be-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="299be-108">El administrador de formularios puede liberarse ahora si no se va a usar para más activaciones de formulario.</span><span class="sxs-lookup"><span data-stu-id="299be-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="299be-109">Tenga en cuenta que una llamada a **LoadForm** puede tardar algún tiempo porque el administrador de formularios puede tener que instalar los archivos ejecutables del servidor de formularios antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="299be-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="299be-110">Opcionalmente, la aplicación cliente puede preparar [IMAPIViewContext](imapiviewcontextiunknown.md) para controlar las operaciones que pueden hacer que el objeto de formulario cargue el mensaje anterior o siguiente de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="299be-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="299be-111">La aplicación cliente puede usar el método [IMAPIForm:: SetViewContext](imapiform-setviewcontext.md) para cambiar el contexto de la vista predeterminada que se estableció en la llamada de **LoadForm** .</span><span class="sxs-lookup"><span data-stu-id="299be-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="299be-112">La aplicación cliente llama al método [IPersistMessage:: Load](ipersistmessage-load.md) para cargar los datos de mensaje en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="299be-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="299be-113">La aplicación cliente llama a [IMAPIForm::D overb](imapiform-doverb.md) para invocar el verbo abrir, pasando el puntero de interfaz [IMAPIViewContext](imapiviewcontextiunknown.md) opcional.</span><span class="sxs-lookup"><span data-stu-id="299be-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="299be-114">Ver también</span><span class="sxs-lookup"><span data-stu-id="299be-114">See also</span></span>



[<span data-ttu-id="299be-115">InterAcciones del servidor de formularios</span><span class="sxs-lookup"><span data-stu-id="299be-115">Form Server Interactions</span></span>](form-server-interactions.md)

