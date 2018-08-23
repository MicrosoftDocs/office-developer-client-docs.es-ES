---
title: Cargar un mensaje en un formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6e65311187ba96abde31a4779ebba371b3d02084
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576501"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="5b848-103">Cargar un mensaje en un formulario</span><span class="sxs-lookup"><span data-stu-id="5b848-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="5b848-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b848-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b848-105">Para cargar un mensaje existente en un formulario mediante un servidor de formulario, utilice una de las siguientes estrategias.</span><span class="sxs-lookup"><span data-stu-id="5b848-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="5b848-106">[IMAPISession:: PrepareForm](imapisession-prepareform.md) para crear un token de llamadas y, a continuación, [IMAPISession:: ShowForm](imapisession-showform.md) para mostrar el formulario.</span><span class="sxs-lookup"><span data-stu-id="5b848-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="5b848-107">Llame a [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span><span class="sxs-lookup"><span data-stu-id="5b848-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="5b848-108">Uso de la estrategia de **PrepareForm** y **ShowForm** es tan fácil, pero da como resultado de los formularios que son modales con respecto a su cliente.</span><span class="sxs-lookup"><span data-stu-id="5b848-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="5b848-109">Esto es debido a que la llamada a **ShowForm** no devuelve hasta que haya salido el formulario.</span><span class="sxs-lookup"><span data-stu-id="5b848-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="5b848-110">Si necesita administrar formularios de forma asincrónica, no use esta estrategia.</span><span class="sxs-lookup"><span data-stu-id="5b848-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="5b848-111">Uso de la estrategia de **LoadForm** es más difícil debido a que el método requiere varios parámetros.</span><span class="sxs-lookup"><span data-stu-id="5b848-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="5b848-112">Estos parámetros instruir al administrador de formulario para iniciar el servidor de formulario correcto en el contexto adecuado y mostrar el mensaje adecuado.</span><span class="sxs-lookup"><span data-stu-id="5b848-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="5b848-113">Si ya se está ejecutando el servidor de formulario, el Administrador de formularios de carga el mensaje en el servidor de formulario sin necesidad de iniciar una nueva instancia del servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="5b848-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="5b848-114">Para especificar qué servidor de formulario para iniciar, pase la clase de mensaje controlada por el servidor de destino en el contenido del parámetro _lpszMessageClass_ .</span><span class="sxs-lookup"><span data-stu-id="5b848-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="5b848-115">La clase de mensaje adecuado se puede determinar mediante la recuperación de la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) del mensaje que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="5b848-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="5b848-116">En ocasiones, no hay ningún servidor de formulario para la clase de mensaje especificado, sólo el servidor de un formulario administra los mensajes que pertenecen a la superclase del mensaje.</span><span class="sxs-lookup"><span data-stu-id="5b848-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="5b848-117">Si prefiere que el mensaje se puede cargar sólo por un servidor de formulario diseñado específicamente para administrar los mensajes de esa clase, establezca el indicador MAPIFORM_EXACTMATCH en la llamada **LoadForm** .</span><span class="sxs-lookup"><span data-stu-id="5b848-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="5b848-118">Para obtener más información, vea [Las clases de mensajes de MAPI](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="5b848-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="5b848-119">**LoadForm** también requiere un puntero al sitio de mensaje del su visor y contexto de vista y el valor para el mensaje de destino **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) y **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) Propiedades.</span><span class="sxs-lookup"><span data-stu-id="5b848-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

