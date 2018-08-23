---
title: Muestra iconos de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7ac8026489b06031e07ab4b2978c9ece04063bb1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579147"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="9a8bc-103">Muestra iconos de formulario</span><span class="sxs-lookup"><span data-stu-id="9a8bc-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="9a8bc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a8bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a8bc-105">Cuando se muestra una lista de mensajes en una carpeta, es útil para los usuarios distinguir los mensajes con clases de mensaje personalizadas desde el formulario estándar IPM. Tenga en cuenta los mensajes.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="9a8bc-106">Clases de mensaje personalizadas se corresponden con los servidores de formulario y los servidores de formulario proporcionan iconos para representar a sí mismos.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="9a8bc-107">Puede mostrar estos iconos en la lista de mensajes de alerta a los usuarios a la clase de mensaje de cada mensaje antes de que el usuario abre los mensajes.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="9a8bc-108">Normalmente, el icono de la propiedad del formulario **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) es el que deben mostrarse en la lista de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="9a8bc-109">Formularios también tienen una propiedad de **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) que se puede mostrar cuando el formulario está minimizado en una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="9a8bc-110">**Para obtener un icono para una clase de mensaje sin activar el servidor de formulario para esa clase de mensaje**</span><span class="sxs-lookup"><span data-stu-id="9a8bc-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="9a8bc-111">Llame al método [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) para obtener un puntero a un [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="9a8bc-112">Llame al método [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) para obtener un puntero a un [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="9a8bc-113">Llame al método [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) para obtener un identificador de icono.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="9a8bc-114">A continuación, se muestra el icono con la API de Win32 estándar.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9a8bc-115">Una vez que el icono de una clase de mensaje, asegúrese de todos los esfuerzos para almacenar en caché ese icono.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="9a8bc-116">No almacenar en caché los iconos gravemente afecta al rendimiento de las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="9a8bc-117">Al almacenar en caché los iconos, tenga cuidado de las relaciones entre las clases de mensajes y sus subclases.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="9a8bc-118">Por ejemplo, si el formulario IPM. Clase de mensaje Note.Meeting.Cancel sucede resolver en IPM. Tenga en cuenta, no asuma que todas las subclases de IPM. Nota debe usar el icono para IPM. Tenga en cuenta.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

