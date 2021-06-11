---
title: Mostrar iconos de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438634"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="0909c-103">Mostrar iconos de formulario</span><span class="sxs-lookup"><span data-stu-id="0909c-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="0909c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0909c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0909c-105">Al mostrar una lista de mensajes en una carpeta, resulta útil para los usuarios si distingue los mensajes con clases de mensajes personalizadas del IPM estándar. Nota de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="0909c-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="0909c-106">Las clases de mensajes personalizadas corresponden a servidores de formulario y los servidores de formulario proporcionan iconos para representarse a sí mismos.</span><span class="sxs-lookup"><span data-stu-id="0909c-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="0909c-107">Puede mostrar estos iconos en la lista de mensajes para alertar a los usuarios de la clase de mensaje de cada mensaje antes de que el usuario abra los mensajes.</span><span class="sxs-lookup"><span data-stu-id="0909c-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="0909c-108">Normalmente, el icono de la propiedad PR_MINI_ICON **(** [PidTagMiniIcon](pidtagminiicon-canonical-property.md)) del formulario es el que debe mostrarse en la lista de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0909c-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="0909c-109">Los formularios **también tienen una PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) que se puede mostrar cuando el formulario se minimiza en una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0909c-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="0909c-110">**Para obtener un icono para una clase de mensaje sin activar el servidor de formularios para esa clase de mensaje**</span><span class="sxs-lookup"><span data-stu-id="0909c-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="0909c-111">Llame al [método IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) para obtener un puntero a una [interfaz IMAPIFormContainer : IUnknown.](imapiformcontaineriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="0909c-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="0909c-112">Llama al [método IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) para obtener un puntero a una [interfaz IMAPIFormInfo : IMAPIProp.](imapiforminfoimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="0909c-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="0909c-113">Llama al [método IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) para obtener un identificador de icono.</span><span class="sxs-lookup"><span data-stu-id="0909c-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="0909c-114">A continuación, el icono se puede mostrar con las API estándar de Win32.</span><span class="sxs-lookup"><span data-stu-id="0909c-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="0909c-115">Una vez que tenga el icono para una clase de mensaje, haga todo lo posible para almacenar en caché ese icono.</span><span class="sxs-lookup"><span data-stu-id="0909c-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="0909c-116">No almacenar en caché iconos afecta gravemente al rendimiento de las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="0909c-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="0909c-117">Al almacenar en caché iconos, tenga cuidado con las relaciones entre las clases de mensaje y sus subclases.</span><span class="sxs-lookup"><span data-stu-id="0909c-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="0909c-118">Por ejemplo, si el IPM. La clase de mensaje Note.Meeting.Cancel vuelve a resolverse en IPM. Tenga en cuenta que no se supone que todas las subclases de IPM. Tenga en cuenta que debe usar el icono de IPM. Nota.</span><span class="sxs-lookup"><span data-stu-id="0909c-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

