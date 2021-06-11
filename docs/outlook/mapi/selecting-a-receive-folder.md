---
title: Selección de una carpeta de recepción
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9151b76f74dead5cac771dbdc091bbee03359aec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428420"
---
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="1f571-103">Selección de una carpeta de recepción</span><span class="sxs-lookup"><span data-stu-id="1f571-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="1f571-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f571-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f571-105">Una carpeta de recepción es donde se colocan los mensajes entrantes de una clase determinada.</span><span class="sxs-lookup"><span data-stu-id="1f571-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="1f571-106">Para ipm y mensajes de informe relacionados, MAPI asigna la Bandeja de entrada como carpeta de recepción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1f571-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="1f571-107">Para IPC y mensajes de informe relacionados, MAPI asigna la carpeta raíz del almacén de mensajes como la carpeta de recepción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1f571-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="1f571-108">Puede cambiar estas asignaciones o realizar asignaciones adicionales para otras clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="1f571-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="1f571-109">Realizar asignaciones explícitas de carpetas de recepción para las clases de mensaje admitidas del cliente es opcional.</span><span class="sxs-lookup"><span data-stu-id="1f571-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="1f571-110">Cuando una clase de mensaje entrante no tiene asignada una carpeta de recepción, el proveedor del almacén de mensajes usa automáticamente la carpeta de recepción para la clase que coincide con el prefijo más largo posible de la clase entrante.</span><span class="sxs-lookup"><span data-stu-id="1f571-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="1f571-111">Por ejemplo, si el cliente recibe un mensaje de clase IPM. Note.MyDocument y la única carpeta de recepción que se ha establecido es la Bandeja de entrada para mensajes IPM, este mensaje se colocará en la Bandeja de entrada porque IPM. Note.MyDocument deriva de la clase base IPM.</span><span class="sxs-lookup"><span data-stu-id="1f571-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="1f571-112">Al asignar una carpeta de recepción para mensajes IPC, nunca use una carpeta del subárbol IPM.</span><span class="sxs-lookup"><span data-stu-id="1f571-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="1f571-113">Estas carpetas deben reservarse solo para mensajes IPM.</span><span class="sxs-lookup"><span data-stu-id="1f571-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="1f571-114">Use en su lugar una carpeta que esté incluida en la carpeta raíz del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1f571-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="1f571-115">**Para crear una carpeta de recepción para una clase de mensaje IPM**</span><span class="sxs-lookup"><span data-stu-id="1f571-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="1f571-116">Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1f571-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="1f571-117">Llama [a IMsgStore::OpenEntry](imsgstore-openentry.md) con **PR_IPM_SUBTREE_ENTRYID** como identificador de entrada para abrir la carpeta raíz del subárbol IPM en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1f571-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="1f571-118">Llama [a IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para crear la carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="1f571-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="1f571-119">Llama [a IMsgStore::SetReceiveFolder para](imsgstore-setreceivefolder.md) asignar la nueva carpeta a la clase de mensaje IPM.</span><span class="sxs-lookup"><span data-stu-id="1f571-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="1f571-120">**Para crear una carpeta de recepción para una clase de mensaje IPC**</span><span class="sxs-lookup"><span data-stu-id="1f571-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="1f571-121">Llama [a IMsgStore::OpenEntry con](imsgstore-openentry.md) un identificador de entrada nulo para abrir la carpeta raíz del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1f571-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="1f571-122">Llama [a IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para crear la carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="1f571-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="1f571-123">Llama [a IMsgStore::SetReceiveFolder para](imsgstore-setreceivefolder.md) asignar la nueva carpeta a la clase de mensaje IPC.</span><span class="sxs-lookup"><span data-stu-id="1f571-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="1f571-124">Asigna la carpeta de recepción que usas para los mensajes de los mensajes de informe relacionados.</span><span class="sxs-lookup"><span data-stu-id="1f571-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="1f571-125">Por ejemplo, si el cliente recibe IPM. Tenga en cuenta los mensajes, configure una carpeta de recepción para el IPM futuro. Tenga en cuenta los mensajes y la misma carpeta de recepción para futuros mensajes Report.IPM.Note.</span><span class="sxs-lookup"><span data-stu-id="1f571-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

