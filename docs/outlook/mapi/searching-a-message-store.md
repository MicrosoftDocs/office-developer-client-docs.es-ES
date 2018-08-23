---
title: Búsqueda de un almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 74b63719f6d72e3c92cbcef6fdb26ee106d4b9aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571839"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="3949b-103">Búsqueda de un almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="3949b-103">Searching a message store</span></span>

<span data-ttu-id="3949b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3949b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3949b-105">Pueden buscar las aplicaciones cliente a través de una o varias carpetas busca los mensajes que coinciden con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3949b-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="3949b-106">La técnica más sencilla de búsqueda implica la aplicación de una restricción para definir los criterios y colocar los resultados en una carpeta de resultados de búsqueda, crea explícitamente para esta búsqueda o para una búsqueda anterior.</span><span class="sxs-lookup"><span data-stu-id="3949b-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="3949b-107">No todos los almacenes de mensajes admiten esta técnica.</span><span class="sxs-lookup"><span data-stu-id="3949b-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="3949b-108">Para determinar si el almacén de mensajes que utiliza admite el uso de las carpetas de resultados de búsqueda, llame a su método [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar la **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) (propiedad).</span><span class="sxs-lookup"><span data-stu-id="3949b-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="3949b-109">Si se establece la marca STORE_SEARCH_OK, se admite la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3949b-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="3949b-110">Si no está establecido, necesitará un planteamiento alternativo como la inspección manualmente las carpetas de destino.</span><span class="sxs-lookup"><span data-stu-id="3949b-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="3949b-111">Para buscar una o varias carpetas en un almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="3949b-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="3949b-112">Si tiene una carpeta de resultados de búsqueda de una búsqueda anterior, vaya al paso 2.</span><span class="sxs-lookup"><span data-stu-id="3949b-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="3949b-113">En caso contrario, para crear una carpeta de resultados de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="3949b-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="3949b-114">Recuperar el identificador de entrada de la carpeta raíz de resultados de búsqueda, llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes y solicite **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3949b-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="3949b-115">Llame a [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir la carpeta representada por PR_FINDER_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="3949b-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="3949b-116">Llamar al método [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) de la carpeta para crear una carpeta de resultados de búsqueda con el conjunto de marca FOLDER_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="3949b-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="3949b-117">Crear una restricción para retener el criterio de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3949b-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="3949b-118">Crear una matriz de identificadores de entrada que representan las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3949b-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="3949b-119">Este paso es necesario si la carpeta de resultados de búsqueda se ha utilizado antes y desea que las mismas carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3949b-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="3949b-120">Llamar al método [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) de la carpeta de resultados de búsqueda, apuntar _lpContainerList_ a la matriz de identificador de entrada y _lpRestriction_ a la restricción.</span><span class="sxs-lookup"><span data-stu-id="3949b-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="3949b-121">Si se ha registrado para las notificaciones de búsqueda completa con el almacén de mensajes, espere a que la notificación llegar.</span><span class="sxs-lookup"><span data-stu-id="3949b-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="3949b-122">Ver los resultados de la búsqueda mediante una llamada a los resultados de búsqueda (método) [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta para tener acceso a su tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="3949b-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="3949b-123">Llamar el contenido [IMAPITable:: QueryRows](imapitable-queryrows.md) al método de la tabla para recuperar los mensajes que cumplen los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3949b-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

