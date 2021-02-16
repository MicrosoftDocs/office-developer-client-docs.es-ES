---
title: Acerca del registro de almacenes para indización
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321829"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="50b9f-103">Acerca del registro de almacenes para indización</span><span class="sxs-lookup"><span data-stu-id="50b9f-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="50b9f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50b9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50b9f-105">Este tema es específico de la búsqueda instantánea en Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="50b9f-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="50b9f-106">La búsqueda instantánea le permite buscar rápidamente elementos en Outlook.</span><span class="sxs-lookup"><span data-stu-id="50b9f-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="50b9f-107">Usa componentes de Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="50b9f-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="50b9f-108">El controlador de protocolo MAPI comprueba en el Registro de Windows los almacenes que debe indizar con fines de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="50b9f-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="50b9f-109">Los proveedores de la Tienda que deban indizarse deben estar registrados en el Registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="50b9f-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="50b9f-110">De forma predeterminada, La búsqueda en el escritorio de Windows agrega los siguientes cuatro tipos de proveedores de almacenamiento al Registro de Windows para permitir la indización:</span><span class="sxs-lookup"><span data-stu-id="50b9f-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="50b9f-111">Almacenar archivos de carpetas personales (. PST).</span><span class="sxs-lookup"><span data-stu-id="50b9f-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="50b9f-112">Almacén de Microsoft Exchange, incluidos los archivos de carpetas sin conexión (.ost).</span><span class="sxs-lookup"><span data-stu-id="50b9f-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="50b9f-113">Almacén de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="50b9f-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="50b9f-114">Almacenar para Microsoft Office Outlook Connector para MSN.</span><span class="sxs-lookup"><span data-stu-id="50b9f-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="50b9f-115">Los proveedores de almacenamiento de terceros que deban indizarse deben registrarse en el Registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="50b9f-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="50b9f-116">Los administradores y usuarios pueden usar una configuración de directiva de grupo para evitar que la búsqueda en el escritorio de Windows indexe elementos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="50b9f-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="50b9f-117">Para obtener más información, consulta [Extender la búsqueda en el escritorio de Windows.](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50b9f-117">For more information, see [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="50b9f-118">Claves del Registro</span><span class="sxs-lookup"><span data-stu-id="50b9f-118">Registry Keys</span></span>

<span data-ttu-id="50b9f-119">En un equipo, todos los proveedores de almacén que deban indizarse deben registrarse solo en una de las tres claves del Registro siguientes en el Registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="50b9f-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="50b9f-120">El controlador de protocolo MAPI busca debajo de cada una de estas claves en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="50b9f-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="50b9f-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search</span><span class="sxs-lookup"><span data-stu-id="50b9f-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search</span></span>\
    
2. <span data-ttu-id="50b9f-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences</span><span class="sxs-lookup"><span data-stu-id="50b9f-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences</span></span>\
    
3. <span data-ttu-id="50b9f-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences</span><span class="sxs-lookup"><span data-stu-id="50b9f-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences</span></span>\
    
 <span data-ttu-id="50b9f-124">Cada valor de la clave corresponde a un proveedor de almacén que se indizaría.</span><span class="sxs-lookup"><span data-stu-id="50b9f-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="50b9f-125">El nombre del valor es el identificador único global (GUID) del proveedor del almacén, que es del tipo **DWORD** y tiene el valor hexadecimal 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="50b9f-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="50b9f-126">GUID para proveedores de la Tienda</span><span class="sxs-lookup"><span data-stu-id="50b9f-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="50b9f-127">La propiedad MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** especifica el GUID de un almacén MAPI.</span><span class="sxs-lookup"><span data-stu-id="50b9f-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="50b9f-128">Los GUID de los proveedores de almacenamiento que índices de Outlook se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="50b9f-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="50b9f-129">**Tipo de proveedor de la Tienda**</span><span class="sxs-lookup"><span data-stu-id="50b9f-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="50b9f-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="50b9f-130">**GUID**</span></span> <br/> |<span data-ttu-id="50b9f-131">**Notas**</span><span class="sxs-lookup"><span data-stu-id="50b9f-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="50b9f-132">Archivos de carpetas personales (. PST)</span><span class="sxs-lookup"><span data-stu-id="50b9f-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="50b9f-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="50b9f-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="50b9f-134">El GUID se documenta en el archivo de encabezado público mspst.h como **MSPST_UID_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="50b9f-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="50b9f-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="50b9f-135">Exchange</span></span>  <br/> |<span data-ttu-id="50b9f-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="50b9f-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="50b9f-137">EL GUID se documenta en el archivo de encabezado público edkmdb.h **como pbExchangeProviderPrimaryUserGuid**</span><span class="sxs-lookup"><span data-stu-id="50b9f-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="50b9f-138">Carpetas públicas</span><span class="sxs-lookup"><span data-stu-id="50b9f-138">Public folders</span></span>  <br/> |<span data-ttu-id="50b9f-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="50b9f-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="50b9f-140">EL GUID se documenta en el archivo de encabezado público edkmdb.h **como pbExchangeProviderPublicGuid**</span><span class="sxs-lookup"><span data-stu-id="50b9f-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="50b9f-141">Conector de Outlook para MSN</span><span class="sxs-lookup"><span data-stu-id="50b9f-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="50b9f-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="50b9f-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="50b9f-143">Ninguno</span><span class="sxs-lookup"><span data-stu-id="50b9f-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50b9f-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="50b9f-144">See also</span></span>



[<span data-ttu-id="50b9f-145">Información sobre la API del almacén</span><span class="sxs-lookup"><span data-stu-id="50b9f-145">About the Store API</span></span>](about-the-store-api.md)

