---
title: Seleccionar una carpeta de recepción
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 87f8b4f4011e405d9848f12b5cae56f27fff1ab8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820599"
---
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="52da1-103">Seleccionar una carpeta de recepción</span><span class="sxs-lookup"><span data-stu-id="52da1-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="52da1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52da1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52da1-105">Una carpeta de recepción es donde se colocan los mensajes entrantes de una clase determinada.</span><span class="sxs-lookup"><span data-stu-id="52da1-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="52da1-106">Para IPM y los mensajes de informe relacionados, MAPI asigna la Bandeja de entrada, como el valor predeterminado de recepción carpeta.</span><span class="sxs-lookup"><span data-stu-id="52da1-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="52da1-107">Para IPC y los mensajes de informe relacionados, MAPI asigna la carpeta raíz del almacén de mensajes, como el valor predeterminado de recepción carpeta.</span><span class="sxs-lookup"><span data-stu-id="52da1-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="52da1-108">Puede cambiar estas asignaciones o realizar asignaciones adicionales para otras clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="52da1-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="52da1-109">Realizar explícita de recepción las asignaciones de carpeta de su cliente compatibles mensaje clases es opcional.</span><span class="sxs-lookup"><span data-stu-id="52da1-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="52da1-110">Cuando una clase de mensaje entrante no tiene una carpeta de recepción asignado, el proveedor de almacén de mensajes utiliza automáticamente la carpeta de recepción para la clase que coincide con el prefijo más largo posible de la clase entrante.</span><span class="sxs-lookup"><span data-stu-id="52da1-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="52da1-111">Por ejemplo, si el cliente recibe un mensaje de clase IPM. Recibe Note.MyDocument y la única carpeta que se ha establecido es la Bandeja de entrada para los mensajes IPM, este mensaje se colocará en la Bandeja de entrada porque IPM. Note.MyDocument se deriva de la clase base IPM.</span><span class="sxs-lookup"><span data-stu-id="52da1-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="52da1-112">Cuando se asigna una carpeta de recepción de mensajes IPC, nunca use una carpeta desde el subárbol IPM.</span><span class="sxs-lookup"><span data-stu-id="52da1-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="52da1-113">Estas carpetas se deben reservarse IPM sólo para mensajes.</span><span class="sxs-lookup"><span data-stu-id="52da1-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="52da1-114">Use en su lugar una carpeta que se encuentra dentro de la carpeta raíz del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="52da1-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="52da1-115">**Para crear una carpeta de recepción para una clase de mensaje IPM**</span><span class="sxs-lookup"><span data-stu-id="52da1-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="52da1-116">Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="52da1-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="52da1-117">Llamar a [IMsgStore::OpenEntry](imsgstore-openentry.md) con **PR_IPM_SUBTREE_ENTRYID** como el identificador de entrada para abrir la carpeta raíz del subárbol IPM en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="52da1-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="52da1-118">Llame a [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para crear la carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="52da1-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="52da1-119">Llame a [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para asignar la nueva carpeta a su clase de mensaje IPM.</span><span class="sxs-lookup"><span data-stu-id="52da1-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="52da1-120">**Para crear una carpeta de recepción para una clase de mensaje IPC**</span><span class="sxs-lookup"><span data-stu-id="52da1-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="52da1-121">Llame al método [IMsgStore::OpenEntry](imsgstore-openentry.md) con un identificador de entrada null para abrir la carpeta raíz del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="52da1-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="52da1-122">Llame a [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para crear la carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="52da1-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="52da1-123">Llame a [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para asignar la nueva carpeta a su clase de mensaje IPC.</span><span class="sxs-lookup"><span data-stu-id="52da1-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="52da1-124">Asignar la carpeta de recepción que usa para los mensajes para los mensajes de informe relacionados.</span><span class="sxs-lookup"><span data-stu-id="52da1-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="52da1-125">Por ejemplo, si el cliente recibe IPM. Los mensajes de nota, configurar una carpeta de recepción para futura IPM. Los mensajes de nota y el mismo reciben carpeta para los mensajes futuros de Report.IPM.Note.</span><span class="sxs-lookup"><span data-stu-id="52da1-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

