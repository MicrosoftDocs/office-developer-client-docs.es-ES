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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 27db5f54f6a6feba77308a4a63fe4c16448550cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817740"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="27d63-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="27d63-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="27d63-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27d63-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27d63-105">Obtiene información sobre lo que puede admitir un almacén se basa en el selector especificado.</span><span class="sxs-lookup"><span data-stu-id="27d63-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="27d63-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27d63-106">Parameters</span></span>

 <span data-ttu-id="27d63-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="27d63-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="27d63-108">[entrada] Selector que indica qué capacidades para devolver.</span><span class="sxs-lookup"><span data-stu-id="27d63-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="27d63-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27d63-109">Return value</span></span>

<span data-ttu-id="27d63-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="27d63-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="27d63-111">Compatibilidad con páginas principales de carpeta en un almacén no predeterminado.</span><span class="sxs-lookup"><span data-stu-id="27d63-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="27d63-112">Puede devolverse si no se especifica **MSCAP_SEL_FOLDER** en *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="27d63-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="27d63-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="27d63-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="27d63-114">Si una restricción contiene cualquier argumento no válido, como las propiedades no válidas, el almacén de pasa por alto los argumentos no válidos y procesa sólo los argumentos válidos.</span><span class="sxs-lookup"><span data-stu-id="27d63-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="27d63-115">Puede devolverse si no se especifica **MSCAP_SEL_RESTRICTION** en *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="27d63-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="27d63-116">NULL</span><span class="sxs-lookup"><span data-stu-id="27d63-116">NULL</span></span>
  
> <span data-ttu-id="27d63-117">El almacén no es compatible con ninguna capacidad basada en el selector de determinado.</span><span class="sxs-lookup"><span data-stu-id="27d63-117">The store does not support any capability based on the given selector.</span></span>
    

