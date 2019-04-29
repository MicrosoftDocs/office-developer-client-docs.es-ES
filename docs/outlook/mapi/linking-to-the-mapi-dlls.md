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
ms.openlocfilehash: 394537a60f4cb9603024115ccea67570291d8ac6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419306"
---
# <a name="linking-to-the-mapi-dlls"></a><span data-ttu-id="4b79c-103">Vincular a las DLL de MAPI</span><span class="sxs-lookup"><span data-stu-id="4b79c-103">Linking to the MAPI DLLs</span></span>

  
  
<span data-ttu-id="4b79c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b79c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b79c-105">Los clientes MAPI se pueden vincular a las dll de MAPI implícita o explícitamente mediante las funciones de Windows **LoadLibrary** y **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="4b79c-105">MAPI clients can link to the MAPI DLLs implicitly, or explicitly by using the Windows functions **LoadLibrary** and **GetProcAddress**.</span></span> <span data-ttu-id="4b79c-106">Para obtener información sobre cómo vincular explícitamente dll MAPI, vea [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4b79c-106">For information on explicitly linking MAPI DLLs, see [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
  
<span data-ttu-id="4b79c-107">MAPI proporciona instrucciones de definición de tipo en MAPIX. H para cada una de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="4b79c-107">MAPI provides type definition statements in the MAPIX.H header file for each of the following functions:</span></span>
  
[<span data-ttu-id="4b79c-108">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="4b79c-108">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="4b79c-109">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="4b79c-109">MAPIUninitialize</span></span>](mapiuninitialize.md)
  
[<span data-ttu-id="4b79c-110">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="4b79c-110">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="4b79c-111">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="4b79c-111">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="4b79c-112">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="4b79c-112">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="4b79c-113">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4b79c-113">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4b79c-114">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="4b79c-114">MAPIAdminProfiles</span></span>](mapiadminprofiles.md)
  
<span data-ttu-id="4b79c-115">Use estas definiciones de tipo para llamar correctamente a los puntos de entrada correspondientes si tiene un vínculo explícito a los archivos dll de MAPI.</span><span class="sxs-lookup"><span data-stu-id="4b79c-115">Use these type definitions to correctly call the corresponding entry points if you link explicitly to the MAPI DLLs.</span></span>
  
<span data-ttu-id="4b79c-116">Los proveedores de servicios pueden contener funciones que no sean MAPI (características completamente no relacionadas con MAPI) en su DLL.</span><span class="sxs-lookup"><span data-stu-id="4b79c-116">Service providers can contain non-MAPI functionality — features that are completely unrelated to MAPI — in their DLL.</span></span> <span data-ttu-id="4b79c-117">Si necesita usar estas características, llame a **LoadLibrary** antes de usar el archivo dll y **FreeLibrary** para quitar la dll de la memoria después de su uso.</span><span class="sxs-lookup"><span data-stu-id="4b79c-117">If you need to use these features, call **LoadLibrary** before using the DLL and **FreeLibrary** to remove the DLL from memory after its use.</span></span> <span data-ttu-id="4b79c-118">Debido a que MAPI no reconoce los usos no MAPI de una DLL de proveedor de servicios, no hay ninguna garantía de que el archivo DLL esté disponible cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4b79c-118">Because MAPI is unaware of non-MAPI uses of a service provider DLL, there is no guarantee that the DLL will be available when needed.</span></span> <span data-ttu-id="4b79c-119">MAPI libera una DLL de proveedor de servicios cuando ya no hay clientes con sesiones activas que requieran sus servicios.</span><span class="sxs-lookup"><span data-stu-id="4b79c-119">MAPI releases a service provider DLL when there are no longer any clients with active sessions that require its services.</span></span> 
  

