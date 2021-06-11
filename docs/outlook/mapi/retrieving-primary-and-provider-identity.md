---
title: Recuperación de la identidad principal y del proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430815"
---
# <a name="retrieving-primary-and-provider-identity"></a><span data-ttu-id="33b2e-103">Recuperación de la identidad principal y del proveedor</span><span class="sxs-lookup"><span data-stu-id="33b2e-103">Retrieving Primary and Provider Identity</span></span>

  
  
<span data-ttu-id="33b2e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33b2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33b2e-105">Los proveedores de servicios, normalmente proveedores de libretas de direcciones, tienen la opción de proporcionar una identidad que se puede usar para representar la sesión en una variedad de situaciones.</span><span class="sxs-lookup"><span data-stu-id="33b2e-105">Service providers, typically address book providers, have the option of supplying an identity that can be used to represent the session in a variety of situations.</span></span> <span data-ttu-id="33b2e-106">Tres propiedades describen la identidad de un proveedor:</span><span class="sxs-lookup"><span data-stu-id="33b2e-106">Three properties describe a provider's identity:</span></span>
  
- <span data-ttu-id="33b2e-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33b2e-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span> 
    
- <span data-ttu-id="33b2e-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33b2e-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span> 
    
- <span data-ttu-id="33b2e-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="33b2e-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="33b2e-110">Estas propiedades se establecen en el identificador de entrada, el nombre para mostrar y la clave de búsqueda del objeto de identidad correspondiente, que suele ser un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="33b2e-110">These properties are set to the entry identifier, display name, and search key of the corresponding identity object, which is typically a messaging user.</span></span> <span data-ttu-id="33b2e-111">Los proveedores que suministran una identidad también establecen la marca STATUS_PRIMARY_IDENTITY en su **propiedad PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="33b2e-111">Providers that supply an identity also set the STATUS_PRIMARY_IDENTITY flag in their **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="33b2e-112">Según sus necesidades, puede usar la identidad de un proveedor en particular o la identidad principal para la sesión.</span><span class="sxs-lookup"><span data-stu-id="33b2e-112">Depending on your needs, you might use a particular provider's identity or the primary identity for the session.</span></span> <span data-ttu-id="33b2e-113">También puede usar la identidad de un proveedor para mostrar o recuperar propiedades, como **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="33b2e-113">You can use a provider's identity also for display purposes or to retrieve properties, such as **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span></span> <span data-ttu-id="33b2e-114">**PR_RESOURCE_PATH**, si se establece, contiene la ruta de acceso a los archivos usados o creados por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="33b2e-114">**PR_RESOURCE_PATH**, if set, contains the path to files used or created by the provider.</span></span> <span data-ttu-id="33b2e-115">Recupere la **PR_RESOURCE_PATH** para el proveedor que proporciona la identidad principal cuando desee buscar archivos que pertenezcan al usuario de la sesión.</span><span class="sxs-lookup"><span data-stu-id="33b2e-115">Retrieve the **PR_RESOURCE_PATH** property for the provider supplying the primary identity when you want to locate files that pertain to the user of the session.</span></span> 
  
 <span data-ttu-id="33b2e-116">**Para recuperar la identidad de un proveedor específico**</span><span class="sxs-lookup"><span data-stu-id="33b2e-116">**To retrieve the identity of a specific provider**</span></span>
  
1. <span data-ttu-id="33b2e-117">Llame [a IMAPISession::GetStatusTable para](imapisession-getstatustable.md) obtener acceso a la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="33b2e-117">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="33b2e-118">Cree una restricción mediante una estructura [SPropertyRestriction](spropertyrestriction.md) para que coincida con la columna **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) con el nombre del proveedor especificado.</span><span class="sxs-lookup"><span data-stu-id="33b2e-118">Build a restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match the **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) column with the name of the specified provider.</span></span> 
    
3. <span data-ttu-id="33b2e-119">Llame [a IMAPITable::FindRow](imapitable-findrow.md) para buscar la fila del proveedor.</span><span class="sxs-lookup"><span data-stu-id="33b2e-119">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the provider's row.</span></span> <span data-ttu-id="33b2e-120">La identidad del proveedor se almacenará en la **PR_IDENTITY_ENTRYID,** si existe.</span><span class="sxs-lookup"><span data-stu-id="33b2e-120">The provider's identity will be stored in the **PR_IDENTITY_ENTRYID** column, if it exists.</span></span> 
    
 <span data-ttu-id="33b2e-121">**Para recuperar la identidad principal de una sesión**</span><span class="sxs-lookup"><span data-stu-id="33b2e-121">**To retrieve the primary identity for a session**</span></span>
  
- <span data-ttu-id="33b2e-122">Llame [a IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="33b2e-122">Call [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="33b2e-123">**QueryIdentity** basa la identidad de sesión en la existencia del valor STATUS_PRIMARY_IDENTITY en la columna **PR_RESOURCE_FLAGS** para una de las filas de la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="33b2e-123">**QueryIdentity** bases session identity on the existence of the STATUS_PRIMARY_IDENTITY value in the **PR_RESOURCE_FLAGS** column for one of the rows in the status table.</span></span> <span data-ttu-id="33b2e-124">Si ninguna de las filas de estado tiene este valor establecido, **QueryIdentity** asigna identidad al primer proveedor de servicios que establece las tres PR_IDENTITY propiedades.</span><span class="sxs-lookup"><span data-stu-id="33b2e-124">If none of the status rows have this value set, **QueryIdentity** assigns identity to the first service provider that sets the three PR_IDENTITY properties.</span></span> <span data-ttu-id="33b2e-125">Si ningún proveedor de servicios proporciona una identidad, **QueryIdentity** devuelve MAPI_W_NO_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="33b2e-125">If no service provider supplies an identity, **QueryIdentity** returns MAPI_W_NO_SERVICE.</span></span> <span data-ttu-id="33b2e-126">Cuando esto sucede, debe crear una cadena de caracteres para representar un usuario genérico que pueda servir como identidad principal.</span><span class="sxs-lookup"><span data-stu-id="33b2e-126">When this happens, you should create a character string to represent a generic user that can serve as the primary identity.</span></span> 
    
 <span data-ttu-id="33b2e-127">**Para establecer explícitamente la identidad principal de una sesión**</span><span class="sxs-lookup"><span data-stu-id="33b2e-127">**To explicitly set the primary identity for a session**</span></span>
  
- <span data-ttu-id="33b2e-128">Llame [a IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="33b2e-128">Call [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span></span> <span data-ttu-id="33b2e-129">Pase **mapiuid** para el proveedor de servicios de destino.</span><span class="sxs-lookup"><span data-stu-id="33b2e-129">Pass the **MAPIUID** for the target service provider.</span></span> 
    

