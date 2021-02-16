---
title: Información sobre la API del almacén
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405558"
---
# <a name="about-the-store-api"></a><span data-ttu-id="282f3-103">Información sobre la API del almacén</span><span class="sxs-lookup"><span data-stu-id="282f3-103">About the Store API</span></span>

  
  
<span data-ttu-id="282f3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="282f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="282f3-105">La API de la Tienda proporciona funcionalidades de almacén varias a los proveedores de la tienda.</span><span class="sxs-lookup"><span data-stu-id="282f3-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="282f3-106">Proporciona las siguientes definciones, tipos de datos, propiedades e interfaces.</span><span class="sxs-lookup"><span data-stu-id="282f3-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="282f3-107">Definiciones:</span><span class="sxs-lookup"><span data-stu-id="282f3-107">Definitions:</span></span>
  
- [<span data-ttu-id="282f3-108">Constantes para la API de Store</span><span class="sxs-lookup"><span data-stu-id="282f3-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="282f3-109">Tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="282f3-109">Data types:</span></span>
  
- <span data-ttu-id="282f3-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="282f3-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="282f3-112">Propiedades con nombre:</span><span class="sxs-lookup"><span data-stu-id="282f3-112">Named Properties:</span></span>
  
- <span data-ttu-id="282f3-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="282f3-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="282f3-115">**[Tamaños de las carpetas del servidor de visualización](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="282f3-116">**[Ocultar la opción de actualización de reuniones](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="282f3-117">**[Hacer que el tipo de tienda sea privado](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="282f3-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="282f3-119">Los proveedores de almacenamiento que no requieren ninguna de las funciones ofrecidas por estas propiedades con nombre simplemente pueden ignorarlos y no implementar compatibilidad en la **interfaz IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="282f3-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="282f3-120">Dado que estas propiedades se proporcionan a partir de Microsoft Outlook 2003 Service Pack 1, agregarlas a un almacén en una versión anterior de Microsoft Outlook no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="282f3-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="282f3-121">Se omiten si no existen o si su valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="282f3-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="282f3-122">Propiedades:</span><span class="sxs-lookup"><span data-stu-id="282f3-122">Properties:</span></span>
  
- <span data-ttu-id="282f3-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="282f3-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="282f3-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="282f3-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="282f3-127">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="282f3-127">Interfaces:</span></span>
  
- <span data-ttu-id="282f3-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="282f3-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="282f3-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="282f3-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="282f3-131">Registro de almacenes para indización</span><span class="sxs-lookup"><span data-stu-id="282f3-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="282f3-132">El controlador de protocolo MAPI comprueba en el Registro de Windows los almacenes que debe indizar con fines de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="282f3-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="282f3-133">Los proveedores de la Tienda que deban indizarse deben estar registrados en el Registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="282f3-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="282f3-134">Para obtener más información acerca del registro de proveedores de almacenamiento para la indización en Outlook 2013 o Outlook 2010, vea Acerca del registro de almacenes para [indización.](about-registering-stores-for-indexing.md)</span><span class="sxs-lookup"><span data-stu-id="282f3-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="282f3-135">Almacenes de indización</span><span class="sxs-lookup"><span data-stu-id="282f3-135">Indexing Stores</span></span>

<span data-ttu-id="282f3-136">Los proveedores de almacén MAPI pueden permitir que el controlador de protocolo MAPI rastree e indexe mensajes en el almacén o envíe notificaciones al indizador solo cuando haya mensajes que se van a indizar.</span><span class="sxs-lookup"><span data-stu-id="282f3-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="282f3-137">Para obtener más información acerca de la indización basada en notificaciones, consulta Acerca [Notification-Based indexación de la Tienda.](about-notification-based-store-indexing.md)</span><span class="sxs-lookup"><span data-stu-id="282f3-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

