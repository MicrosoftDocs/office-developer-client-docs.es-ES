---
title: Exposici�n de las carpetas de almacenes de mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 62f50ed7925305eca7432da17130d2be0365ef03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582598"
---
# <a name="exposing-folders-in-message-stores"></a><span data-ttu-id="fa9f4-103">Exposici�n de las carpetas de almacenes de mensaje</span><span class="sxs-lookup"><span data-stu-id="fa9f4-103">Exposing Folders in Message Stores</span></span>

  
  
<span data-ttu-id="fa9f4-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa9f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa9f4-p101">Cada proveedor de almac�n de mensajes debe presentar una interfaz de [IMAPIFolder](imapifolderimapicontainer.md) de nivel superior a las aplicaciones cliente. La carpeta de nivel superior se corresponde con el almac�n de todo el mensaje; proporciona acceso a las carpetas que los usuarios ven como el contenido del almac�n de mensajes. Adem�s, la carpeta de nivel superior se usa a menudo como el valor predeterminado de recepci�n carpeta para los mensajes IPC y como la carpeta desde la que se env�an los informes de lectura. Los proveedores de almac�n de mensajes tambi�n deben presentar un sub�rbol IPM, un conjunto de carpetas que se usa para contener los mensajes de IPM: a las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-p101">Every message store provider must present a top-level [IMAPIFolder](imapifolderimapicontainer.md) interface to client applications. The top-level folder corresponds to the entire message store; it provides access to the folders that users see as the contents of the message store. In addition, the top-level folder is often used as the default receive folder for IPC messages and as the folder from which read reports are sent. Message store providers must also present an IPM subtree — a set of folders used to contain IPM messages — to client applications.</span></span> 
  
<span data-ttu-id="fa9f4-p102">Las aplicaciones cliente pueden abrir la carpeta de nivel superior mediante una llamada al m�todo de [IMsgStore::OpenEntry](imsgstore-openentry.md) con 0 y NULL para los par�metros  _cbEntryId_ y  _lpEntryId_, respectivamente. Sin embargo, en la mayor�a de los casos, las aplicaciones cliente de abran el conjunto de carpetas que contienen los mensajes de IPM.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-p102">Client applications can open the top-level folder by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with 0 and NULL for the  _cbEntryId_ and  _lpEntryId_ parameters, respectively. In most cases, however, client applications open the set of folders that contain IPM messages.</span></span> 
  
<span data-ttu-id="fa9f4-111">Para obtener una lista de carpetas en el �rbol de carpetas del almac�n de mensaje IPM, utilice el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="fa9f4-111">To get a list of folders in the message store's IPM folder tree, use the following procedure:</span></span>
  
1. <span data-ttu-id="fa9f4-112">Utilice la sesi�n de MAPI para llamar al m�todo [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="fa9f4-112">Use your MAPI session to call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> 
    
2. <span data-ttu-id="fa9f4-113">Use el puntero resultante de base de datos de mensaje para llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) para la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fa9f4-113">Use the resulting message database pointer to call the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="fa9f4-114">Llame al m�todo [IMsgStore::OpenEntry](imsgstore-openentry.md) con el identificador de entrada para obtener un puntero de **IMAPIFolder**.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-114">Call the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with the entry identifier to get an **IMAPIFolder** pointer.</span></span> 
    
4. <span data-ttu-id="fa9f4-115">Llame al m�todo [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) para obtener una tabla de contenido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-115">Call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to get a table of the contents of the folder.</span></span> 
    
5. <span data-ttu-id="fa9f4-116">Llame al m�todo [IMAPITable:: QueryRows](imapitable-queryrows.md) para ver una lista de las carpetas en la carpeta de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-116">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to list the folders in the top-level folder.</span></span> 
    
<span data-ttu-id="fa9f4-p103">Los clientes MAPI utilizan estas carpetas para obtener acceso a otros objetos folder y objetos de mensaje en el almac�n de mensajes. **IMAPIFolder**y su interfaz primaria [IMAPIContainer](imapicontainerimapiprop.md), contienen los m�todos que debe implementar el proveedor de almac�n de mensajes para rellenar las carpetas con objetos de mensaje y responder a las solicitudes de cliente para funcionar en los mensajes.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-p103">MAPI clients use these folders to access other folder objects and message objects in the message store. **IMAPIFolder**, and its parent interface [IMAPIContainer](imapicontainerimapiprop.md), contain the methods your message store provider must implement to populate folders with message objects and respond to client requests to operate on messages.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa9f4-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa9f4-119">See also</span></span>



[<span data-ttu-id="fa9f4-120">Implementar carpetas en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="fa9f4-120">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

