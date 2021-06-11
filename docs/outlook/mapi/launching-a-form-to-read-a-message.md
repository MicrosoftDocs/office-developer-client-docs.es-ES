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
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="0d72f-103">Iniciar un formulario para leer un mensaje</span><span class="sxs-lookup"><span data-stu-id="0d72f-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="0d72f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d72f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d72f-105">Los implementadores del servidor de formularios deben esperar la siguiente secuencia de llamadas de método a su servidor de formulario y objetos de formulario cuando una aplicación cliente carga un mensaje:</span><span class="sxs-lookup"><span data-stu-id="0d72f-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="0d72f-106">La aplicación cliente abre el administrador de formularios con una llamada a la [función MAPIOpenFormMgr.](mapiopenformmgr.md)</span><span class="sxs-lookup"><span data-stu-id="0d72f-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="0d72f-107">La aplicación cliente llama al [método IMAPIFormMgr::LoadForm,](imapiformmgr-loadform.md) que devuelve un objeto [con IMAPIForm](imapiformiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0d72f-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="0d72f-108">El administrador de formularios puede publicarse ahora si no se usará para otras activaciones de formulario.</span><span class="sxs-lookup"><span data-stu-id="0d72f-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="0d72f-109">Tenga en cuenta que una llamada **a LoadForm** puede tardar algún tiempo porque es posible que el administrador de formularios tenga que instalar los archivos ejecutables del servidor de formularios antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="0d72f-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="0d72f-110">Opcionalmente, la aplicación cliente puede preparar [IMAPIViewContext](imapiviewcontextiunknown.md) para controlar las operaciones que pueden hacer que el objeto de formulario cargue el mensaje anterior o siguiente en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0d72f-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="0d72f-111">La aplicación cliente puede usar el método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) para cambiar el contexto de vista predeterminado que se estableció en la **llamada LoadForm.**</span><span class="sxs-lookup"><span data-stu-id="0d72f-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="0d72f-112">La aplicación cliente llama al [método IPersistMessage::Load](ipersistmessage-load.md) para cargar los datos del mensaje en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="0d72f-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="0d72f-113">La aplicación cliente llama [a IMAPIForm::D oVerb](imapiform-doverb.md) para invocar el verbo abierto, pasando el puntero de interfaz [IMAPIViewContext](imapiviewcontextiunknown.md) opcional.</span><span class="sxs-lookup"><span data-stu-id="0d72f-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0d72f-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d72f-114">See also</span></span>



[<span data-ttu-id="0d72f-115">Interacciones del servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="0d72f-115">Form Server Interactions</span></span>](form-server-interactions.md)

