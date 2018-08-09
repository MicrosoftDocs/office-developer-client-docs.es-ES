---
title: Información sobre la API del almacén
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 31aff61ec5868b0f1e9ab34d498b2e8175519f0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816385"
---
# <a name="about-the-store-api"></a><span data-ttu-id="50ba8-103">Información sobre la API del almacén</span><span class="sxs-lookup"><span data-stu-id="50ba8-103">About the Store API</span></span>

  
  
<span data-ttu-id="50ba8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="50ba8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="50ba8-105">La API de almacenar proporciona funcionalidad de almacén de varios para los proveedores de almacén.</span><span class="sxs-lookup"><span data-stu-id="50ba8-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="50ba8-106">Proporciona las siguientes definiciones, propiedades, tipos de datos y las interfaces.</span><span class="sxs-lookup"><span data-stu-id="50ba8-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="50ba8-107">Definiciones:</span><span class="sxs-lookup"><span data-stu-id="50ba8-107">Definitions:</span></span>
  
- [<span data-ttu-id="50ba8-108">Constantes de la API del almacén</span><span class="sxs-lookup"><span data-stu-id="50ba8-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="50ba8-109">Tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="50ba8-109">Data types:</span></span>
  
- <span data-ttu-id="50ba8-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="50ba8-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="50ba8-112">Propiedades con nombre:</span><span class="sxs-lookup"><span data-stu-id="50ba8-112">Named Properties:</span></span>
  
- <span data-ttu-id="50ba8-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="50ba8-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="50ba8-115">**[Mostrar el tamaño de la carpeta de servidor](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="50ba8-116">**[Ocultar la opción de actualización de la reunión](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="50ba8-117">**[Asegúrese de almacén tipo privado](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="50ba8-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="50ba8-119">Los proveedores de almacén que no requieren cualquiera de la funcionalidad proporcionada por estas propiedades con nombre pueden simplemente pasar por alto y no implementar la compatibilidad en la interfaz de **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="50ba8-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="50ba8-120">Debido a que estas propiedades se proporcionan a partir de Microsoft Outlook 2003 Service Pack 1, agregarlos a un almacén en una versión anterior de Microsoft Outlook no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="50ba8-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="50ba8-121">Se omiten si no existen o si su valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="50ba8-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="50ba8-122">Propiedades:</span><span class="sxs-lookup"><span data-stu-id="50ba8-122">Properties:</span></span>
  
- <span data-ttu-id="50ba8-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="50ba8-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="50ba8-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="50ba8-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="50ba8-127">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="50ba8-127">Interfaces:</span></span>
  
- <span data-ttu-id="50ba8-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="50ba8-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="50ba8-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="50ba8-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="50ba8-131">Registrar almacenes para la indización</span><span class="sxs-lookup"><span data-stu-id="50ba8-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="50ba8-132">El controlador de protocolo MAPI comprueba el registro de Windows para los almacenes que deben indizar para fines de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="50ba8-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="50ba8-133">Los proveedores de almacén que desean indizar deben estar registrados en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="50ba8-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="50ba8-134">Para obtener más información acerca de cómo registrar los proveedores de almacén para la indización en Outlook 2013 o Outlook 2010, vea el [Registro de almacenes para la indización](about-registering-stores-for-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="50ba8-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="50ba8-135">Almacenes de indización</span><span class="sxs-lookup"><span data-stu-id="50ba8-135">Indexing Stores</span></span>

<span data-ttu-id="50ba8-136">Pueden elegir los proveedores de almacén MAPI permitir que al controlador de protocolo MAPI a rastrear e indizar los mensajes en el almacén, o enviar notificaciones al indizador sólo cuando hay mensajes que se va a indizar.</span><span class="sxs-lookup"><span data-stu-id="50ba8-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="50ba8-137">Para obtener más información acerca de la indización basada en notificaciones, vea [About Notification-Based almacén de indización](about-notification-based-store-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="50ba8-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

