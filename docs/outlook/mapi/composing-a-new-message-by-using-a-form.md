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
ms.openlocfilehash: f4b9cb00512838e6b54c0cc910b8f7279120db3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816556"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="16bb1-103">Redactar un mensaje nuevo con un formulario</span><span class="sxs-lookup"><span data-stu-id="16bb1-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="16bb1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16bb1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16bb1-105">Para usar un formulario para redactar un mensaje nuevo, en primer lugar hay que crear un nuevo objeto de mensaje personalizado.</span><span class="sxs-lookup"><span data-stu-id="16bb1-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="16bb1-106">**Para redactar un nuevo mensaje mediante un formulario**</span><span class="sxs-lookup"><span data-stu-id="16bb1-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="16bb1-107">Llamar al método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) del director de formulario para recuperar un puntero a un objeto de información de un formulario, un objeto que implementa el [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="16bb1-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="16bb1-108">Pase el puntero al objeto de información de formulario en una llamada a [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span><span class="sxs-lookup"><span data-stu-id="16bb1-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="16bb1-109">**CreateForm** carga el servidor de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="16bb1-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="16bb1-110">Además, puede pasar un identificador de interfaz a **CreateForm** para especificar la interfaz que se usará para tener acceso al mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="16bb1-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="16bb1-111">Normalmente, se solicita [IPersistMessage: IUnknown](ipersistmessageiunknown.md) pasando IID_IPersistMessage al **CreateForm**.</span><span class="sxs-lookup"><span data-stu-id="16bb1-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="16bb1-112">Guarde el nuevo mensaje mediante una llamada a su método [IPersistMessage::Save](ipersistmessage-save.md) .</span><span class="sxs-lookup"><span data-stu-id="16bb1-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="16bb1-113">El servidor de formulario debe establecer los valores de las propiedades del mensaje necesarios cuando crea el mensaje.</span><span class="sxs-lookup"><span data-stu-id="16bb1-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="16bb1-114">Cargar el mensaje mediante uno de dos estrategias: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) o [IMAPISession:: PrepareForm](imapisession-prepareform.md) seguido [IMAPISession:: ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="16bb1-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="16bb1-115">Para obtener más información acerca de estas estrategias, vea [cargar un mensaje en un formulario](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="16bb1-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="16bb1-116">Existen oportunidades de ganancias en el rendimiento al cargar un nuevo mensaje personalizado en un servidor de formulario porque ya habrá tenía una oportunidad para obtener información acerca del mensaje, como su clase de mensaje: durante el procesamiento necesario para la ** ResolveMessageClass** y **CreateForm** llamadas.</span><span class="sxs-lookup"><span data-stu-id="16bb1-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="16bb1-117">Por este motivo, podrá simplificar el procesamiento necesario antes de llamar a **LoadForm** a través de la se describe en el tema [al cargar un mensaje en un formulario](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="16bb1-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

