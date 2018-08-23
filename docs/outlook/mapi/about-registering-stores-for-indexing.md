---
title: Información sobre el registro de almacenes de indexación
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 195812f53c4c0aaf20e4ed6e215d15b0295c9a07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584187"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="680b5-103">Información sobre el registro de almacenes de indexación</span><span class="sxs-lookup"><span data-stu-id="680b5-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="680b5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="680b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="680b5-105">En este tema es específico para la búsqueda instantánea de Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="680b5-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="680b5-106">Búsqueda instantánea le permite encontrar rápidamente los elementos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="680b5-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="680b5-107">Utiliza los componentes de Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="680b5-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="680b5-108">El controlador de protocolo MAPI comprueba el registro de Windows para los almacenes que deben indizar para fines de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="680b5-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="680b5-109">Los proveedores de almacén que desean indizar deben estar registrados en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="680b5-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="680b5-110">De forma predeterminada, Windows Desktop Search agrega los siguientes cuatro tipos de los proveedores de almacén para el registro de Windows para permitir la indización:</span><span class="sxs-lookup"><span data-stu-id="680b5-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="680b5-111">Almacén de archivos de carpetas personales (. PST).</span><span class="sxs-lookup"><span data-stu-id="680b5-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="680b5-112">Almacén de Microsoft Exchange, incluidos los archivos de carpetas sin conexión (.ost).</span><span class="sxs-lookup"><span data-stu-id="680b5-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="680b5-113">Almacén de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="680b5-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="680b5-114">Almacén para Microsoft Office Outlook Connector para MSN.</span><span class="sxs-lookup"><span data-stu-id="680b5-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="680b5-115">Los proveedores de almacén de otro fabricante que desean que se indice deben registrarse en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="680b5-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="680b5-116">Los administradores y usuarios pueden usar una configuración de directiva de grupo para impedir la indización de los elementos de Outlook de Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="680b5-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="680b5-117">Para obtener más información, vea [Ampliación de Windows Desktop Search](http://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="680b5-117">For more information, see [Extending Windows Desktop Search](http://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="680b5-118">Claves del registro</span><span class="sxs-lookup"><span data-stu-id="680b5-118">Registry Keys</span></span>

<span data-ttu-id="680b5-119">En un equipo, todos los proveedores de almacén que desean indizar deben estar registrados en sólo uno de los siguientes tres claves del registro en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="680b5-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="680b5-120">El controlador de protocolo MAPI tiene el aspecto bajo cada una de estas claves en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="680b5-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="680b5-121">\Software\Policies\Microsoft\Windows\Windows Search\ [HKLM]</span><span class="sxs-lookup"><span data-stu-id="680b5-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search\\</span></span>
    
2. <span data-ttu-id="680b5-122">\Software\Microsoft\Windows\Windows Search\Preferences\ [HKLM]</span><span class="sxs-lookup"><span data-stu-id="680b5-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
3. <span data-ttu-id="680b5-123">\Software\Microsoft\Windows\Windows Search\Preferences\ [HKCU]</span><span class="sxs-lookup"><span data-stu-id="680b5-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
 <span data-ttu-id="680b5-124">Cada valor en la clave corresponde a un proveedor de almacén que se van a indizar.</span><span class="sxs-lookup"><span data-stu-id="680b5-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="680b5-125">El nombre del valor es el identificador único global (GUID) del proveedor de almacenamiento, que es del tipo **DWORD** y tiene el valor hexadecimal 0 x 00000001.</span><span class="sxs-lookup"><span data-stu-id="680b5-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="680b5-126">GUID de los proveedores de almacén</span><span class="sxs-lookup"><span data-stu-id="680b5-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="680b5-127">La propiedad MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** especifica el GUID de un almacén de MAPI.</span><span class="sxs-lookup"><span data-stu-id="680b5-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="680b5-128">Los GUID para los proveedores de almacén de que los índices de Outlook se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="680b5-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="680b5-129">**Tipo de proveedor de almacenamiento**</span><span class="sxs-lookup"><span data-stu-id="680b5-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="680b5-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="680b5-130">**GUID**</span></span> <br/> |<span data-ttu-id="680b5-131">**Notas**</span><span class="sxs-lookup"><span data-stu-id="680b5-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="680b5-132">Archivos de carpetas personales (. (PST)</span><span class="sxs-lookup"><span data-stu-id="680b5-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="680b5-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="680b5-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="680b5-134">GUID se documenta en el mspst.h del archivo de encabezado público como **MSPST_UID_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="680b5-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="680b5-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="680b5-135">Exchange</span></span>  <br/> |<span data-ttu-id="680b5-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="680b5-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="680b5-137">GUID se documenta en el edkmdb.h del archivo de encabezado público como **pbExchangeProviderPrimaryUserGuid**</span><span class="sxs-lookup"><span data-stu-id="680b5-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="680b5-138">Carpetas públicas</span><span class="sxs-lookup"><span data-stu-id="680b5-138">Public folders</span></span>  <br/> |<span data-ttu-id="680b5-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="680b5-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="680b5-140">GUID se documenta en el edkmdb.h del archivo de encabezado público como **pbExchangeProviderPublicGuid**</span><span class="sxs-lookup"><span data-stu-id="680b5-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="680b5-141">Outlook Connector para MSN</span><span class="sxs-lookup"><span data-stu-id="680b5-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="680b5-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="680b5-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="680b5-143">Ninguno</span><span class="sxs-lookup"><span data-stu-id="680b5-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="680b5-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="680b5-144">See also</span></span>



[<span data-ttu-id="680b5-145">Información sobre la API del almacén</span><span class="sxs-lookup"><span data-stu-id="680b5-145">About the Store API</span></span>](about-the-store-api.md)

