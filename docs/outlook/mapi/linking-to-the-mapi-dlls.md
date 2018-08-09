---
title: Vincular a las DLL de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0bce1d682057b81135d1684c40bc79e6710d4e2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818019"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="6c7bc-103">Vincular a las DLL de MAPI</span><span class="sxs-lookup"><span data-stu-id="6c7bc-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="6c7bc-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6c7bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6c7bc-105">Los clientes MAPI pueden vincular a las DLL MAPI implícitamente o explícitamente mediante el uso de las funciones de Windows **LoadLibrary** y **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="6c7bc-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="6c7bc-106">Para obtener información sobre la vinculación de forma explícita dll MAPI, vea el [vínculo a las funciones de MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6c7bc-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="6c7bc-107">MAPI proporciona instrucciones de definición de tipo en el MAPIX. Archivo de encabezado de H para cada una de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="6c7bc-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="6c7bc-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="6c7bc-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="6c7bc-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="6c7bc-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="6c7bc-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="6c7bc-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="6c7bc-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="6c7bc-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="6c7bc-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="6c7bc-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="6c7bc-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6c7bc-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6c7bc-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="6c7bc-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="6c7bc-115">Use estas definiciones de tipo para llamar correctamente a los puntos de entrada correspondiente si vincula explícitamente a la DLL de MAPI.</span><span class="sxs-lookup"><span data-stu-id="6c7bc-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="6c7bc-116">Proveedores de servicios pueden contener funcionalidad que no sean MAPI: las características que no están completamente relacionadas a MAPI: en su archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="6c7bc-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="6c7bc-117">Si necesita usar estas características, llame a **LoadLibrary** antes de usar el archivo DLL y **FreeLibrary** para quitar el archivo DLL de la memoria después de su uso.</span><span class="sxs-lookup"><span data-stu-id="6c7bc-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="6c7bc-118">Debido a que no tiene constancia de usos de MAPI que no sean de un proveedor de servicios de DLL MAPI, no hay ninguna garantía de que el archivo DLL estará disponible cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="6c7bc-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="6c7bc-119">MAPI libera un archivo DLL del proveedor de servicios cuando ya no hay ningún clientes con las sesiones activas que requieren sus servicios.</span><span class="sxs-lookup"><span data-stu-id="6c7bc-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

