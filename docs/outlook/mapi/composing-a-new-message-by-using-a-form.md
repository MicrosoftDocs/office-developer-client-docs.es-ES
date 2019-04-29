---
title: Redactar un mensaje nuevo con un formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412803"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="13431-103">Redactar un mensaje nuevo con un formulario</span><span class="sxs-lookup"><span data-stu-id="13431-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="13431-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13431-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13431-105">Para usar un formulario para redactar un nuevo mensaje, primero debe crear un nuevo objeto de mensaje personalizado.</span><span class="sxs-lookup"><span data-stu-id="13431-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="13431-106">**Para redactar un mensaje nuevo con un formulario**</span><span class="sxs-lookup"><span data-stu-id="13431-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="13431-107">Llame al método [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) del administrador de formularios para recuperar un puntero a un objeto de información de formulario (un objeto que implementa la interfaz [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="13431-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="13431-108">Pase el puntero al objeto de información del formulario en una llamada a [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md).</span><span class="sxs-lookup"><span data-stu-id="13431-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="13431-109">**CreateForm** carga el servidor de formularios apropiado.</span><span class="sxs-lookup"><span data-stu-id="13431-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="13431-110">Además, pase un identificador de interfaz a **CreateForm** para especificar la interfaz que se va a usar para obtener acceso al nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="13431-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="13431-111">Normalmente, se solicita [IPersistMessage: IUnknown](ipersistmessageiunknown.md) pasando IID_IPersistMessage a **CreateForm**.</span><span class="sxs-lookup"><span data-stu-id="13431-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="13431-112">Guarde el nuevo mensaje llamando a su método [IPersistMessage:: Save](ipersistmessage-save.md) .</span><span class="sxs-lookup"><span data-stu-id="13431-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="13431-113">El servidor de formularios debe establecer los valores de las propiedades requeridas del mensaje al crear el mensaje.</span><span class="sxs-lookup"><span data-stu-id="13431-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="13431-114">Cargue el mensaje con una de estas dos estrategias: [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) o [IMAPISession::P Repareform](imapisession-prepareform.md) seguida de [IMAPISession:: ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="13431-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="13431-115">Para obtener más información acerca de estas estrategias, consulte [cargar un mensaje en un formulario](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="13431-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="13431-116">Existen oportunidades para mejorar el rendimiento cuando se carga un nuevo mensaje personalizado en un servidor de formularios porque ya se ha tenido la oportunidad de obtener información sobre el mensaje (por ejemplo, su clase de mensaje) durante el procesamiento necesario para el \*\* \*\*Llamadas a ResolveMessageClass y **CreateForm** .</span><span class="sxs-lookup"><span data-stu-id="13431-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="13431-117">Por este motivo, podrá simplificar el procesamiento necesario antes de llamar a **LoadForm** sobre lo que se describe en el tema [cargar un mensaje en un formulario](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="13431-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

