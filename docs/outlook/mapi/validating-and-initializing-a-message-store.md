---
title: Validación e inicialización de un almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 48883ec33db9ffd6b3e7cc6e16ae9c2487a31607
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820978"
---
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="c75dc-103">Validación e inicialización de un almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="c75dc-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="c75dc-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c75dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c75dc-105">Cuando se abre un almacén de mensajes a través del método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) sin establecer la marca MDB_NO_MAIL, MAPI crea varias carpetas y se les asigna roles y los nombres predeterminados.</span><span class="sxs-lookup"><span data-stu-id="c75dc-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="c75dc-106">MAPI es responsable de la creación de estas carpetas para evitar las incompatibilidades que inevitablemente se produciría si los clientes o los proveedores de almacén de mensajes fueron los responsables de la creación.</span><span class="sxs-lookup"><span data-stu-id="c75dc-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="c75dc-107">En ocasiones, es necesario comprobar que se han creado las carpetas correspondientes y que son válidos.</span><span class="sxs-lookup"><span data-stu-id="c75dc-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="c75dc-108">La función [HrValidateIPMSubtree](hrvalidateipmsubtree.md) está disponible para este propósito.</span><span class="sxs-lookup"><span data-stu-id="c75dc-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="c75dc-109">Si se está validando el almacén de mensajes de forma predeterminada, pase el indicador MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="c75dc-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="c75dc-110">Se crea un grupo más amplio de carpetas para el almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c75dc-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="c75dc-111">Cuando **HrValidateIPMSubtree** recibe el indicador MAPI_FULL_IPM_TREE, busca las siguientes carpetas:</span><span class="sxs-lookup"><span data-stu-id="c75dc-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="c75dc-112">Carpeta raíz para el subárbol IPM</span><span class="sxs-lookup"><span data-stu-id="c75dc-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="c75dc-113">Carpeta Elementos eliminados en la carpeta raíz IPM</span><span class="sxs-lookup"><span data-stu-id="c75dc-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="c75dc-114">Carpeta Bandeja de entrada en la carpeta raíz IPM</span><span class="sxs-lookup"><span data-stu-id="c75dc-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="c75dc-115">Carpeta en la carpeta raíz IPM Bandeja de salida</span><span class="sxs-lookup"><span data-stu-id="c75dc-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="c75dc-116">Carpeta Elementos enviados en la carpeta raíz IPM</span><span class="sxs-lookup"><span data-stu-id="c75dc-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="c75dc-117">Vistas de la carpeta en la carpeta raíz del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="c75dc-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="c75dc-118">Vistas comunes en la carpeta raíz del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="c75dc-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="c75dc-119">Carpeta de búsqueda en la carpeta raíz del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="c75dc-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="c75dc-120">Si el almacén de mensajes no es el valor predeterminado, puede establecer o no establecer la marca MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="c75dc-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="c75dc-121">Cuando esta marca no está establecida, **HrValidateIPMSubtree** comprueba sólo la carpeta raíz del subárbol, la carpeta Elementos eliminados y la carpeta raíz de mensaje almacenan los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c75dc-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="c75dc-122">Para inicializar un almacén de mensajes, almacenar las siguientes propiedades en la memoria para que estén disponibles:</span><span class="sxs-lookup"><span data-stu-id="c75dc-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="c75dc-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c75dc-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="c75dc-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c75dc-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="c75dc-125">Estas propiedades son máscaras de bits que describen las características del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c75dc-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="c75dc-126">**PR_VALID_FOLDER_MASK** tiene un bit establecido para cada carpeta especial que existe en el almacén de mensajes y tiene un identificador de entrada asignados que es válido.</span><span class="sxs-lookup"><span data-stu-id="c75dc-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="c75dc-127">Para obtener más información acerca del acceso a estas carpetas y sus identificadores de entrada, vea [Abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="c75dc-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="c75dc-128">**PR_STORE_SUPPORT_MASK** tiene un bit establecido para cada característica admitida en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c75dc-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="c75dc-129">Por ejemplo, si es compatible con un almacén de mensajes de notificación y texto con formato, su **PR_STORE_SUPPORT_MASK** tendrá el conjunto de bits STORE_NOTIFY_OK y STORE_RTF_OK.</span><span class="sxs-lookup"><span data-stu-id="c75dc-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="c75dc-130">Otras propiedades que se almacenen localmente incluyen los identificadores de entrada para las carpetas que se describe la propiedad **PR_VALID_FOLDER_MASK** como válido.</span><span class="sxs-lookup"><span data-stu-id="c75dc-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="c75dc-131">Cada una de estas carpetas especiales, excepto la carpeta Bandeja de entrada, tiene una propiedad de identificador de entrada asociada con él.</span><span class="sxs-lookup"><span data-stu-id="c75dc-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="c75dc-132">Por ejemplo, el identificador de entrada de la carpeta Bandeja de salida es su propiedad **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c75dc-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="c75dc-133">Dado que estas carpetas son las carpetas que se va a abrir con frecuencia, es una buena idea hacer que sus identificadores de entrada disponibles.</span><span class="sxs-lookup"><span data-stu-id="c75dc-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

