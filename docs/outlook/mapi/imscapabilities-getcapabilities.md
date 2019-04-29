---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409261"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="deba9-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="deba9-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="deba9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="deba9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="deba9-105">Obtiene información sobre lo que puede admitir un almacén basándose en el selector especificado.</span><span class="sxs-lookup"><span data-stu-id="deba9-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="deba9-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="deba9-106">Parameters</span></span>

 <span data-ttu-id="deba9-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="deba9-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="deba9-108">a Selector que indica las funcionalidades que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="deba9-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="deba9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="deba9-109">Return value</span></span>

<span data-ttu-id="deba9-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="deba9-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="deba9-111">Compatibilidad con páginas principales de carpeta en un almacén no predeterminado.</span><span class="sxs-lookup"><span data-stu-id="deba9-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="deba9-112">Esto puede devolverse si **MSCAP_SEL_FOLDER** se especifica en *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="deba9-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="deba9-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="deba9-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="deba9-114">Si una restricción contiene algún argumento no válido, como propiedades no válidas, el almacén omite los argumentos no válidos y procesa sólo los argumentos válidos.</span><span class="sxs-lookup"><span data-stu-id="deba9-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="deba9-115">Esto puede devolverse si **MSCAP_SEL_RESTRICTION** se especifica en *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="deba9-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="deba9-116">NULL</span><span class="sxs-lookup"><span data-stu-id="deba9-116">NULL</span></span>
  
> <span data-ttu-id="deba9-117">El almacén no admite ninguna función basada en el selector dado.</span><span class="sxs-lookup"><span data-stu-id="deba9-117">The store does not support any capability based on the given selector.</span></span>
    

