---
title: Información sobre la API del almacén
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321752"
---
# <a name="about-the-store-api"></a><span data-ttu-id="1c618-103">Información sobre la API del almacén</span><span class="sxs-lookup"><span data-stu-id="1c618-103">About the Store API</span></span>

  
  
<span data-ttu-id="1c618-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c618-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c618-105">La API de tienda proporciona funcionalidad de varios almacenes para almacenar proveedores.</span><span class="sxs-lookup"><span data-stu-id="1c618-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="1c618-106">Proporciona las siguientes definiciones, tipos de datos, propiedades e interfaces.</span><span class="sxs-lookup"><span data-stu-id="1c618-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="1c618-107">Definiciones:</span><span class="sxs-lookup"><span data-stu-id="1c618-107">Definitions:</span></span>
  
- [<span data-ttu-id="1c618-108">Constantes para la API de tienda</span><span class="sxs-lookup"><span data-stu-id="1c618-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="1c618-109">Tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="1c618-109">Data types:</span></span>
  
- <span data-ttu-id="1c618-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="1c618-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="1c618-112">Propiedades con nombre:</span><span class="sxs-lookup"><span data-stu-id="1c618-112">Named Properties:</span></span>
  
- <span data-ttu-id="1c618-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="1c618-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="1c618-115">**[Mostrar tamaños de carpeta del servidor](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="1c618-116">**[Ocultar opción de actualización de reunión](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="1c618-117">**[Convertir en privado el tipo de tienda](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="1c618-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="1c618-119">Los proveedores de almacenamiento que no requieran ninguna de las funciones que ofrecen estas propiedades con nombre pueden omitirlos y no implementar la compatibilidad en la interfaz **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="1c618-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="1c618-120">Como estas propiedades se proporcionan a partir de Microsoft Outlook 2003 Service Pack 1, agregarlos a un almacén en una versión anterior de Microsoft Outlook no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="1c618-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="1c618-121">Se omiten si no existen o si su valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="1c618-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="1c618-122">Propiedades:</span><span class="sxs-lookup"><span data-stu-id="1c618-122">Properties:</span></span>
  
- <span data-ttu-id="1c618-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="1c618-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="1c618-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="1c618-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="1c618-127">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="1c618-127">Interfaces:</span></span>
  
- <span data-ttu-id="1c618-128">**[A ifoldersupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="1c618-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="1c618-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="1c618-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="1c618-131">Registro de almacenes para la indización</span><span class="sxs-lookup"><span data-stu-id="1c618-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="1c618-132">El controlador de protocolo MAPI busca en el registro de Windows los almacenes que debe indizar para fines de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1c618-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="1c618-133">Los proveedores de almacenamiento que deseen indizar deben registrarse en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="1c618-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="1c618-134">Para obtener más información sobre el registro de los proveedores de almacenamiento para la indización en Outlook 2013 o Outlook 2010, consulte [About registraTion Stores for Indexing](about-registering-stores-for-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="1c618-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="1c618-135">Indización de almacenes</span><span class="sxs-lookup"><span data-stu-id="1c618-135">Indexing Stores</span></span>

<span data-ttu-id="1c618-136">Los proveedores de almacén MAPI pueden elegir permitir que el controlador del protocolo MAPI rastree e indizar mensajes en el almacén, o enviar notificaciones al indizador sólo cuando hay mensajes que se van a indizar.</span><span class="sxs-lookup"><span data-stu-id="1c618-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="1c618-137">Para obtener más información acerca de la indexación basada en notificaciones, consulte [About Notification-based Store Indexing](about-notification-based-store-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="1c618-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

