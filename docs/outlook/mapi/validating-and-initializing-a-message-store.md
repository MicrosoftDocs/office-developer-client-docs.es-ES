---
title: Validar e inicializar un almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 77b3f707fc36a868de5acd7c7ba4642a1da4e3c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329585"
---
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="771d7-103">Validar e inicializar un almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="771d7-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="771d7-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="771d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="771d7-105">Cuando abre un almacén de mensajes mediante el método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) sin establecer la marca MDB_NO_MAIL, MAPI crea varias carpetas y les asigna nombres y roles predeterminados.</span><span class="sxs-lookup"><span data-stu-id="771d7-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="771d7-106">MAPI es responsable de crear estas carpetas para evitar las incompatibilidades que se producirían inevitablemente si los clientes o los proveedores de almacenamiento de mensajes eran responsables de la creación.</span><span class="sxs-lookup"><span data-stu-id="771d7-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="771d7-107">A veces es necesario comprobar que se han creado las carpetas adecuadas y que son válidas.</span><span class="sxs-lookup"><span data-stu-id="771d7-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="771d7-108">La función [HrValidateIPMSubtree](hrvalidateipmsubtree.md) está disponible para este propósito.</span><span class="sxs-lookup"><span data-stu-id="771d7-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="771d7-109">Si va a validar el almacén de mensajes predeterminado, pase la marca MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="771d7-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="771d7-110">Se crea un grupo de carpetas más amplio para el almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="771d7-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="771d7-111">Cuando **HrValidateIPMSubtree** recibe la marca MAPI_FULL_IPM_TREE, comprueba las siguientes carpetas:</span><span class="sxs-lookup"><span data-stu-id="771d7-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="771d7-112">Carpeta raíz para el subárbol IPM</span><span class="sxs-lookup"><span data-stu-id="771d7-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="771d7-113">Carpeta elementos eliminados en la carpeta raíz de IPM</span><span class="sxs-lookup"><span data-stu-id="771d7-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="771d7-114">Carpeta Bandeja de entrada en la carpeta raíz IPM</span><span class="sxs-lookup"><span data-stu-id="771d7-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="771d7-115">Carpeta Bandeja de salida en la carpeta raíz IPM</span><span class="sxs-lookup"><span data-stu-id="771d7-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="771d7-116">Carpeta elementos enviados en la carpeta raíz de IPM</span><span class="sxs-lookup"><span data-stu-id="771d7-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="771d7-117">Vistas de carpeta en la carpeta raíz del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="771d7-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="771d7-118">Vistas comunes en la carpeta raíz del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="771d7-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="771d7-119">Carpeta de búsqueda en la carpeta raíz del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="771d7-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="771d7-120">Si el almacén de mensajes no es el predeterminado, puede establecer o no la marca MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="771d7-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="771d7-121">Si no se establece este indicador, **HrValidateIPMSubtree** comprueba sólo la carpeta raíz del subárbol, la carpeta elementos eliminados y la carpeta raíz para los resultados de la búsqueda del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="771d7-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="771d7-122">Para inicializar un almacén de mensajes, almacene las siguientes propiedades en la memoria para que estén disponibles fácilmente:</span><span class="sxs-lookup"><span data-stu-id="771d7-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="771d7-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="771d7-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="771d7-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="771d7-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="771d7-125">Estas propiedades son máscaras de máscaras que describen las características del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="771d7-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="771d7-126">**PR_VALID_FOLDER_MASK** tiene un bit establecido para cada carpeta especial que existe en el almacén de mensajes y tiene un identificador de entrada asignado que es válido.</span><span class="sxs-lookup"><span data-stu-id="771d7-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="771d7-127">Para obtener más información acerca de cómo tener acceso a estas carpetas y sus identificadores de entrada, consulte [abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="771d7-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="771d7-128">**PR_STORE_SUPPORT_MASK** tiene un bit establecido para cada característica admitida en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="771d7-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="771d7-129">Por ejemplo, si un almacén de mensajes admite la notificación y el texto con formato, su **PR_STORE_SUPPORT_MASK** tendrá establecidos los bits STORE_NOTIFY_OK y STORE_RTF_OK.</span><span class="sxs-lookup"><span data-stu-id="771d7-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="771d7-130">Otras propiedades que deben almacenarse de forma local incluyen los identificadores de entrada de las carpetas que la propiedad **PR_VALID_FOLDER_MASK** describe como válidas.</span><span class="sxs-lookup"><span data-stu-id="771d7-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="771d7-131">Cada una de estas carpetas especiales, excepto la carpeta Bandeja de entrada, tiene asociada una propiedad de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="771d7-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="771d7-132">Por ejemplo, el identificador de entrada de la carpeta Bandeja de salida es su propiedad **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="771d7-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="771d7-133">Como estas carpetas son las carpetas que se abrirán con frecuencia, es aconsejable que sus identificadores de entrada estén disponibles fácilmente.</span><span class="sxs-lookup"><span data-stu-id="771d7-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

