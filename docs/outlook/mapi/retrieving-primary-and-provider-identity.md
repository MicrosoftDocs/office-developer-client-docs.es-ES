---
title: Recuperar identidades de proveedor y principales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: da11cf684c4bdcfb94d33791ed7c61d2e322e1a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586588"
---
# <a name="retrieving-primary-and-provider-identity"></a><span data-ttu-id="bf572-103">Recuperar identidades de proveedor y principales</span><span class="sxs-lookup"><span data-stu-id="bf572-103">Retrieving Primary and Provider Identity</span></span>

  
  
<span data-ttu-id="bf572-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf572-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf572-105">Proveedores de servicios, normalmente proveedores de libreta de direcciones, tienen la opción de proporcionar una identidad que puede usarse para representar la sesión en una gran variedad de situaciones.</span><span class="sxs-lookup"><span data-stu-id="bf572-105">Service providers, typically address book providers, have the option of supplying an identity that can be used to represent the session in a variety of situations.</span></span> <span data-ttu-id="bf572-106">Tres propiedades describen la identidad de un proveedor:</span><span class="sxs-lookup"><span data-stu-id="bf572-106">Three properties describe a provider's identity:</span></span>
  
- <span data-ttu-id="bf572-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf572-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span> 
    
- <span data-ttu-id="bf572-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf572-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span> 
    
- <span data-ttu-id="bf572-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf572-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="bf572-110">Estas propiedades se establecen en el identificador de entrada, el nombre para mostrar y la clave de búsqueda del objeto identity correspondiente, que normalmente es un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="bf572-110">These properties are set to the entry identifier, display name, and search key of the corresponding identity object, which is typically a messaging user.</span></span> <span data-ttu-id="bf572-111">Proveedores que suministran una identidad también establecer la marca STATUS_PRIMARY_IDENTITY en su propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bf572-111">Providers that supply an identity also set the STATUS_PRIMARY_IDENTITY flag in their **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="bf572-112">Dependiendo de sus necesidades, podría usar la identidad de un determinado proveedor o la identidad principal para la sesión.</span><span class="sxs-lookup"><span data-stu-id="bf572-112">Depending on your needs, you might use a particular provider's identity or the primary identity for the session.</span></span> <span data-ttu-id="bf572-113">Puede usar la identidad de un proveedor también para fines de presentación o para recuperar las propiedades, como **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bf572-113">You can use a provider's identity also for display purposes or to retrieve properties, such as **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span></span> <span data-ttu-id="bf572-114">**PR_RESOURCE_PATH**, si establece, contiene la ruta de acceso a archivos usa o creada por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="bf572-114">**PR_RESOURCE_PATH**, if set, contains the path to files used or created by the provider.</span></span> <span data-ttu-id="bf572-115">Recupere la propiedad **PR_RESOURCE_PATH** para el proveedor de proporcionar la identidad principal cuando desea ubicar los archivos que pertenecen al usuario de la sesión.</span><span class="sxs-lookup"><span data-stu-id="bf572-115">Retrieve the **PR_RESOURCE_PATH** property for the provider supplying the primary identity when you want to locate files that pertain to the user of the session.</span></span> 
  
 <span data-ttu-id="bf572-116">**Para recuperar la identidad de un proveedor específico**</span><span class="sxs-lookup"><span data-stu-id="bf572-116">**To retrieve the identity of a specific provider**</span></span>
  
1. <span data-ttu-id="bf572-117">Llame a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="bf572-117">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="bf572-118">Crear una restricción de uso de una estructura de [SPropertyRestriction](spropertyrestriction.md) para que coincida con la columna **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) con el nombre del proveedor especificado.</span><span class="sxs-lookup"><span data-stu-id="bf572-118">Build a restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match the **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) column with the name of the specified provider.</span></span> 
    
3. <span data-ttu-id="bf572-119">Llamar a [IMAPITable:: FindRow](imapitable-findrow.md) para localizar fila del proveedor en la.</span><span class="sxs-lookup"><span data-stu-id="bf572-119">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the provider's row.</span></span> <span data-ttu-id="bf572-120">Identidad del proveedor se almacenará en la columna **PR_IDENTITY_ENTRYID** , si existe.</span><span class="sxs-lookup"><span data-stu-id="bf572-120">The provider's identity will be stored in the **PR_IDENTITY_ENTRYID** column, if it exists.</span></span> 
    
 <span data-ttu-id="bf572-121">**Para recuperar la identidad principal para una sesión**</span><span class="sxs-lookup"><span data-stu-id="bf572-121">**To retrieve the primary identity for a session**</span></span>
  
- <span data-ttu-id="bf572-122">Llame a [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="bf572-122">Call [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="bf572-123">**QueryIdentity** bases de identidad de la sesión de la existencia del valor STATUS_PRIMARY_IDENTITY en la columna **PR_RESOURCE_FLAGS** de una de las filas de la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="bf572-123">**QueryIdentity** bases session identity on the existence of the STATUS_PRIMARY_IDENTITY value in the **PR_RESOURCE_FLAGS** column for one of the rows in the status table.</span></span> <span data-ttu-id="bf572-124">Si ninguna de las filas de estado tienen definido este valor, **QueryIdentity** asigna la identidad para el primer proveedor de servicios que establece las tres propiedades PR_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="bf572-124">If none of the status rows have this value set, **QueryIdentity** assigns identity to the first service provider that sets the three PR_IDENTITY properties.</span></span> <span data-ttu-id="bf572-125">Si ningún proveedor de servicio proporciona una identidad, **QueryIdentity** devuelve MAPI_W_NO_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="bf572-125">If no service provider supplies an identity, **QueryIdentity** returns MAPI_W_NO_SERVICE.</span></span> <span data-ttu-id="bf572-126">Cuando esto sucede, debe crear una cadena de caracteres para representar un usuario genérico que puede servir como la identidad principal.</span><span class="sxs-lookup"><span data-stu-id="bf572-126">When this happens, you should create a character string to represent a generic user that can serve as the primary identity.</span></span> 
    
 <span data-ttu-id="bf572-127">**Para establecer explícitamente la identidad principal para una sesión**</span><span class="sxs-lookup"><span data-stu-id="bf572-127">**To explicitly set the primary identity for a session**</span></span>
  
- <span data-ttu-id="bf572-128">Llame a [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="bf572-128">Call [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span></span> <span data-ttu-id="bf572-129">Pase el **MAPIUID** para el proveedor de servicio de destino.</span><span class="sxs-lookup"><span data-stu-id="bf572-129">Pass the **MAPIUID** for the target service provider.</span></span> 
    

