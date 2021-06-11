---
title: Propiedad Display Server Folder Sizes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434553"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="b6f67-103">Propiedad Display Server Folder Sizes</span><span class="sxs-lookup"><span data-stu-id="b6f67-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="b6f67-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6f67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6f67-105">Muestra los tamaños de las carpetas especificadas en el servidor en el cuadro de diálogo Outlook **tamaño de** carpeta.</span><span class="sxs-lookup"><span data-stu-id="b6f67-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b6f67-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b6f67-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6f67-107">Expuesto en:</span><span class="sxs-lookup"><span data-stu-id="b6f67-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="b6f67-108">[IMsgStore : objeto IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="b6f67-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="b6f67-109">Creado por:</span><span class="sxs-lookup"><span data-stu-id="b6f67-109">Created by:</span></span>  <br/> |<span data-ttu-id="b6f67-110">Proveedor de la tienda</span><span class="sxs-lookup"><span data-stu-id="b6f67-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="b6f67-111">Al que se accede mediante:</span><span class="sxs-lookup"><span data-stu-id="b6f67-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="b6f67-112">Outlook y otros clientes</span><span class="sxs-lookup"><span data-stu-id="b6f67-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="b6f67-113">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="b6f67-113">Property type:</span></span>  <br/> |<span data-ttu-id="b6f67-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b6f67-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b6f67-115">Tipo de acceso:</span><span class="sxs-lookup"><span data-stu-id="b6f67-115">Access type:</span></span>  <br/> |<span data-ttu-id="b6f67-116">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b6f67-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6f67-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b6f67-117">Remarks</span></span>

<span data-ttu-id="b6f67-118">Para proporcionar cualquiera de las funciones del almacén, el proveedor de la tienda debe implementar [IMAPIProp : IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válida para cualquiera de estas propiedades pasadas a una llamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="b6f67-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="b6f67-119">Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de propiedad correcto.</span><span class="sxs-lookup"><span data-stu-id="b6f67-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="b6f67-120">Los proveedores de almacenamiento [pueden llamar a HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp para](hrsetoneprop.md) obtener o establecer estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b6f67-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="b6f67-121">Para recuperar el valor de esta propiedad, el cliente primero debe usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="b6f67-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="b6f67-122">Al llamar [a IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) apuntada por el parámetro de entrada  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="b6f67-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6f67-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="b6f67-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="b6f67-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="b6f67-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="b6f67-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="b6f67-125">ulKind:</span></span>  <br/> |<span data-ttu-id="b6f67-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="b6f67-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="b6f67-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="b6f67-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="b6f67-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span><span class="sxs-lookup"><span data-stu-id="b6f67-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="b6f67-129">Esta propiedad se admite en Microsoft Outlook 2003 Service Pack (SP) 1.</span><span class="sxs-lookup"><span data-stu-id="b6f67-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="b6f67-130">Si la versión de Outlook es anterior a Outlook 2003 SP 1 o si su valor es **false,** Outlook mostrará solo los tamaños de carpetas en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="b6f67-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="b6f67-131">Si esta propiedad se establece en un almacén que usa Outlook 2003 SP 1, Outlook consultará el tamaño de cada carpeta especificada en el servidor y la unidad local.</span><span class="sxs-lookup"><span data-stu-id="b6f67-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="b6f67-132">Para consultar el tamaño de carpeta en el servidor, Outlook abre una carpeta en el almacén con [IMsgStore::OpenEntry](imsgstore-openentry.md), pasando la marca **MAPI_NO_CACHE** y, a continuación, consulta **para PR_MESSAGE_SIZE_EXTENDED**.</span><span class="sxs-lookup"><span data-stu-id="b6f67-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="b6f67-133">A continuación, el proveedor de almacenamiento debe devolver el tamaño de carpeta en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b6f67-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="b6f67-134">Para consultar el tamaño de una carpeta en la unidad local, Outlook abre la carpeta sin la **marca MAPI_NO_CACHE.**</span><span class="sxs-lookup"><span data-stu-id="b6f67-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="b6f67-135">A continuación, se consulta **PR_MESSAGE_SIZE_EXTENDED**; el proveedor de almacenamiento debe devolver el tamaño de la carpeta especificada en la unidad local.</span><span class="sxs-lookup"><span data-stu-id="b6f67-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="b6f67-136">Con este conjunto de propiedades, los proveedores de almacenamiento que sincronizan el contenido del almacén con un servidor pueden mostrar datos de tamaño de carpeta en el servidor en el cuadro de diálogo Outlook **tamaño** de carpeta.</span><span class="sxs-lookup"><span data-stu-id="b6f67-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="b6f67-137">A continuación, los usuarios pueden comparar el uso actual del almacenamiento del servidor con las cuotas de servidor.</span><span class="sxs-lookup"><span data-stu-id="b6f67-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

