---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c51f4a7266e67be08f31daa5afbf23ce0b256252
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567856"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="32a20-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="32a20-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="32a20-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32a20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32a20-105">Obtiene información sobre la compatibilidad de una carpeta para compartir.</span><span class="sxs-lookup"><span data-stu-id="32a20-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="32a20-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32a20-106">Parameters</span></span>

 <span data-ttu-id="32a20-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="32a20-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="32a20-108">[out] Una máscara de bits que indica si la carpeta es compatible con el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="32a20-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="32a20-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="32a20-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="32a20-110">Indica que la carpeta no es compatible con el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="32a20-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="32a20-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="32a20-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="32a20-112">Indica que la carpeta es compatible con el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="32a20-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="32a20-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32a20-113">Return value</span></span>

<span data-ttu-id="32a20-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="32a20-114">S_OK</span></span> 
  
> <span data-ttu-id="32a20-115">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="32a20-115">The call was successful.</span></span>
    

