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
ms.openlocfilehash: 0211a326e94c5847c040040e0e0e4e9ddd1d760d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583277"
---
# <a name="imscapabilitiesgetcapabilities"></a><span data-ttu-id="d0371-103">IMSCapabilities::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="d0371-103">IMSCapabilities::GetCapabilities</span></span>

  
  
<span data-ttu-id="d0371-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0371-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0371-105">Obtiene información sobre lo que puede admitir un almacén se basa en el selector especificado.</span><span class="sxs-lookup"><span data-stu-id="d0371-105">Gets information about what a store can support based on the specified selector.</span></span>
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a><span data-ttu-id="d0371-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0371-106">Parameters</span></span>

 <span data-ttu-id="d0371-107">*mscapSelector*</span><span class="sxs-lookup"><span data-stu-id="d0371-107">*mscapSelector*</span></span> 
  
> <span data-ttu-id="d0371-108">[entrada] Selector que indica qué capacidades para devolver.</span><span class="sxs-lookup"><span data-stu-id="d0371-108">[in] Selector indicating which capabilities to return.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d0371-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0371-109">Return value</span></span>

<span data-ttu-id="d0371-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="d0371-110">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>
  
> <span data-ttu-id="d0371-111">Compatibilidad con páginas principales de carpeta en un almacén no predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d0371-111">Support for folder homepages in a non-default store.</span></span> <span data-ttu-id="d0371-112">Puede devolverse si no se especifica **MSCAP_SEL_FOLDER** en *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="d0371-112">This can be returned if **MSCAP_SEL_FOLDER** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="d0371-113">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="d0371-113">MSCAP_RES_ANNOTATION</span></span>
  
> <span data-ttu-id="d0371-114">Si una restricción contiene cualquier argumento no válido, como las propiedades no válidas, el almacén de pasa por alto los argumentos no válidos y procesa sólo los argumentos válidos.</span><span class="sxs-lookup"><span data-stu-id="d0371-114">If a restriction contains any invalid arguments such as invalid properties, the store ignores the invalid arguments and processes only the valid arguments.</span></span> <span data-ttu-id="d0371-115">Puede devolverse si no se especifica **MSCAP_SEL_RESTRICTION** en *mscapSelector* .</span><span class="sxs-lookup"><span data-stu-id="d0371-115">This can be returned if **MSCAP_SEL_RESTRICTION** is specified in  *mscapSelector*  .</span></span> 
    
<span data-ttu-id="d0371-116">NULL</span><span class="sxs-lookup"><span data-stu-id="d0371-116">NULL</span></span>
  
> <span data-ttu-id="d0371-117">El almacén no es compatible con ninguna capacidad basada en el selector de determinado.</span><span class="sxs-lookup"><span data-stu-id="d0371-117">The store does not support any capability based on the given selector.</span></span>
    

