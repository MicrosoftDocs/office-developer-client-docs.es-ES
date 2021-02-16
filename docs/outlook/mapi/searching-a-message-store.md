---
title: Buscar un almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7240f49a15fdaea4d1f30dae578d25c3f2c1c0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426040"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="3a66a-103">Buscar un almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="3a66a-103">Searching a message store</span></span>

<span data-ttu-id="3a66a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a66a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a66a-105">Las aplicaciones cliente pueden buscar en una o más carpetas mensajes que coincidan con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3a66a-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="3a66a-106">La técnica de búsqueda más sencilla implica aplicar una restricción para definir criterios y colocar los resultados en una carpeta de resultados de búsqueda, creada explícitamente para esta búsqueda o para una búsqueda anterior.</span><span class="sxs-lookup"><span data-stu-id="3a66a-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="3a66a-107">No todos los almacenes de mensajes admiten esta técnica.</span><span class="sxs-lookup"><span data-stu-id="3a66a-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="3a66a-108">Para determinar si el almacén de mensajes que está usando admite el uso de carpetas de resultados de búsqueda, llame a su método [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar la propiedad **PR \_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3a66a-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="3a66a-109">Si se STORE_SEARCH_OK marca, se admite la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3a66a-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="3a66a-110">Si no se establece, necesitará un enfoque alternativo, como inspeccionar manualmente las carpetas de destino.</span><span class="sxs-lookup"><span data-stu-id="3a66a-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="3a66a-111">Para buscar una o más carpetas en un almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="3a66a-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="3a66a-112">Si tiene una carpeta de resultados de búsqueda de una búsqueda anterior, vaya directamente al paso 2.</span><span class="sxs-lookup"><span data-stu-id="3a66a-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="3a66a-113">De lo contrario, para crear una carpeta de resultados de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="3a66a-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="3a66a-114">Recupere el identificador de entrada de la carpeta raíz de resultados de búsqueda llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes y solicitando PR_FINDER_ENTRYID **(** [PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3a66a-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="3a66a-115">Llame [a IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir la carpeta representada por PR_FINDER_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="3a66a-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="3a66a-116">Llame al método [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) de la carpeta para crear una carpeta de resultados de búsqueda con el FOLDER_SEARCH marca establecida.</span><span class="sxs-lookup"><span data-stu-id="3a66a-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="3a66a-117">Crear una restricción para contener los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3a66a-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="3a66a-118">Cree una matriz de identificadores de entrada que representen las carpetas en las que buscar.</span><span class="sxs-lookup"><span data-stu-id="3a66a-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="3a66a-119">Este paso no es necesario si la carpeta de resultados de búsqueda se ha usado antes y desea buscar en las mismas carpetas.</span><span class="sxs-lookup"><span data-stu-id="3a66a-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="3a66a-120">Llama al método [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) de la carpeta de resultados de búsqueda,  _apuntando lpContainerList_ a la matriz del identificador de entrada y  _lpRestriction_ a la restricción.</span><span class="sxs-lookup"><span data-stu-id="3a66a-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="3a66a-121">Si se ha registrado para recibir notificaciones completas de búsqueda con el almacén de mensajes, espere a que llegue la notificación.</span><span class="sxs-lookup"><span data-stu-id="3a66a-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="3a66a-122">Para ver los resultados de la búsqueda, llame al método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta de resultados de búsqueda para obtener acceso a su tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="3a66a-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="3a66a-123">Llame al método [IMAPITable::QueryRows](imapitable-queryrows.md) de la tabla de contenido para recuperar los mensajes que cumplen los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3a66a-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

