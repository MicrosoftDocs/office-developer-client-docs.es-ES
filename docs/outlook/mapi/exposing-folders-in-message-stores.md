---
title: Mostrar carpetas en los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 62f50ed7925305eca7432da17130d2be0365ef03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582598"
---
# <a name="exposing-folders-in-message-stores"></a><span data-ttu-id="964f6-103">Mostrar carpetas en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="964f6-103">Exposing Folders in Message Stores</span></span>

  
  
<span data-ttu-id="964f6-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="964f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="964f6-p101">Cada proveedor de almacenes de mensajes debe presentar una interfaz [IMAPIFolder](imapifolderimapicontainer.md) de alto nivel a las aplicaciones cliente. La carpeta de alto nivel se corresponde con el almacén de mensajes completo; proporciona acceso a las carpetas que los usuarios ven como el contenido del almacén de mensajes. Además, la carpeta de alto nivel se utiliza a menudo como la carpeta predeterminada para recibir mensajes IPC y como la carpeta desde la que se envían los informes de lectura. Los proveedores de almacenes de mensajes también deben presentar un subárbol IPM (un conjunto de carpetas que se utilizan para contener mensajes IPM) a las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="964f6-p101">Every message store provider must present a top-level [IMAPIFolder](imapifolderimapicontainer.md) interface to client applications. The top-level folder corresponds to the entire message store; it provides access to the folders that users see as the contents of the message store. In addition, the top-level folder is often used as the default receive folder for IPC messages and as the folder from which read reports are sent. Message store providers must also present an IPM subtree — a set of folders used to contain IPM messages — to client applications.</span></span> 
  
<span data-ttu-id="964f6-p102">Las aplicaciones cliente pueden abrir la carpeta de alto nivel llamando al método [IMsgStore::OpenEntry](imsgstore-openentry.md) con 0 y NULL para los parámetros _cbEntryId_ y _lpEntryId_, respectivamente. Sin embargo, en la mayoría de los casos, las aplicaciones cliente abren el conjunto de carpetas que contienen los mensajes IPM.</span><span class="sxs-lookup"><span data-stu-id="964f6-p102">Client applications can open the top-level folder by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with 0 and NULL for the  _cbEntryId_ and  _lpEntryId_ parameters, respectively. In most cases, however, client applications open the set of folders that contain IPM messages.</span></span> 
  
<span data-ttu-id="964f6-111">Para obtener una lista de las carpetas IPM en el árbol de carpetas del almacén de mensajes, siga este procedimiento:</span><span class="sxs-lookup"><span data-stu-id="964f6-111">To get a list of folders in the message store's IPM folder tree, use the following procedure:</span></span>
  
1. <span data-ttu-id="964f6-112">Utilice la sesión MAPI para llamar al método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="964f6-112">Use your MAPI session to call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> 
    
2. <span data-ttu-id="964f6-113">Utilice el puntero de base de datos del mensaje resultante para llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) para la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="964f6-113">Use the resulting message database pointer to call the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the **PR_IPM_SUBTREE_ENTRYID** ( [PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="964f6-114">Llame al método [IMsgStore::OpenEntry](imsgstore-openentry.md) con el identificador de entrada para obtener un puntero **IMAPIFolder**.</span><span class="sxs-lookup"><span data-stu-id="964f6-114">Call the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with the entry identifier to get an **IMAPIFolder** pointer.</span></span> 
    
4. <span data-ttu-id="964f6-115">Llame al método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) para obtener una tabla del contenido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="964f6-115">Call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to get a table of the contents of the folder.</span></span> 
    
5. <span data-ttu-id="964f6-116">Llame al método [IMAPITable::QueryRows](imapitable-queryrows.md) para obtener una lista de las carpetas de la carpeta de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="964f6-116">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to list the folders in the top-level folder.</span></span> 
    
<span data-ttu-id="964f6-p103">Los clientes MAPI usan estas carpetas para obtener acceso a otros objetos de carpeta y objetos mensaje en el almacén de mensajes. **IMAPIFolder** y su interfaz primaria [IMAPIContainer](imapicontainerimapiprop.md) contienen los métodos que debe implementar el proveedor del almacén de mensajes para rellenar las carpetas con objetos de mensajes y responder a solicitudes de cliente para operar en los mensajes.</span><span class="sxs-lookup"><span data-stu-id="964f6-p103">MAPI clients use these folders to access other folder objects and message objects in the message store. **IMAPIFolder**, and its parent interface [IMAPIContainer](imapicontainerimapiprop.md), contain the methods your message store provider must implement to populate folders with message objects and respond to client requests to operate on messages.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="964f6-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="964f6-119">See also</span></span>



[<span data-ttu-id="964f6-120">Implementar carpetas en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="964f6-120">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

