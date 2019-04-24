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
ms.openlocfilehash: afecd3b334dd2cf7b2953916872982e6459a8434
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355751"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="b86a6-103">Cargar un mensaje en un formulario</span><span class="sxs-lookup"><span data-stu-id="b86a6-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="b86a6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b86a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b86a6-105">Para cargar un mensaje existente en un formulario mediante un servidor de formularios, use una de las siguientes estrategias.</span><span class="sxs-lookup"><span data-stu-id="b86a6-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="b86a6-106">Llame a [IMAPISession::P repareform](imapisession-prepareform.md) para crear un token y, a continuación, [IMAPISession:: ShowForm](imapisession-showform.md) para mostrar el formulario.</span><span class="sxs-lookup"><span data-stu-id="b86a6-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="b86a6-107">Llamar a [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md).</span><span class="sxs-lookup"><span data-stu-id="b86a6-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="b86a6-108">El uso de la estrategia **PrepareForm** y **ShowForm** es comparativamente fácil, pero da como resultado formularios que son modales con respecto a su cliente.</span><span class="sxs-lookup"><span data-stu-id="b86a6-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="b86a6-109">Esto se debe a que la llamada a **ShowForm** no devuelve ningún valor hasta que se haya salido del formulario.</span><span class="sxs-lookup"><span data-stu-id="b86a6-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="b86a6-110">Si necesita controlar formularios de forma asincrónica, no use esta estrategia.</span><span class="sxs-lookup"><span data-stu-id="b86a6-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="b86a6-111">El uso de la estrategia **LoadForm** es más difícil porque el método requiere varios parámetros.</span><span class="sxs-lookup"><span data-stu-id="b86a6-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="b86a6-112">Estos parámetros indican al administrador de formularios que inicie el servidor de formularios apropiado en el contexto adecuado y muestre el mensaje correcto.</span><span class="sxs-lookup"><span data-stu-id="b86a6-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="b86a6-113">Si el servidor de formularios ya se está ejecutando, el administrador de formularios carga el mensaje en el servidor de formularios sin iniciar una nueva instancia del servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="b86a6-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="b86a6-114">Para especificar el servidor de formulario que se iniciará, pase la clase de mensaje controlada por el servidor de destino en el contenido del parámetro _lpszMessageClass_ .</span><span class="sxs-lookup"><span data-stu-id="b86a6-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="b86a6-115">La clase de mensaje adecuada puede determinarse recuperando la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) del mensaje que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="b86a6-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="b86a6-116">A veces, no hay ningún servidor de formularios para la clase de mensaje especificada, sólo un servidor de formularios que controla mensajes pertenecientes a la superclase del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b86a6-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="b86a6-117">Si prefiere que el mensaje se cargue solo por un servidor de formularios específicamente diseñado para controlar los mensajes de esa clase, establezca la marca MAPIFORM_EXACTMATCH en la llamada **LoadForm** .</span><span class="sxs-lookup"><span data-stu-id="b86a6-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="b86a6-118">Para obtener más información, consulte [clases de mensajes MAPI](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="b86a6-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="b86a6-119"><b0>LoadForm</b0> también requiere un puntero al sitio de mensajes del visor y al contexto de la vista, y al valor de los <b1>PR_MSG_STATUS</b1> (<b2>PidTagMessageStatus</b2>) y <b3>PR_MESSAGE_FLAGS</b3> (<b4>PidTagMessageFlags</b4>) del mensaje de destino. </a1>.</span><span class="sxs-lookup"><span data-stu-id="b86a6-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

