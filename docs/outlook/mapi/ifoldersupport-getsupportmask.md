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
ms.openlocfilehash: 6f7aa23606da40c817c9af623b8bade9383ce427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817190"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="da87b-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="da87b-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="da87b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da87b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da87b-105">Obtiene información sobre la compatibilidad de una carpeta para compartir.</span><span class="sxs-lookup"><span data-stu-id="da87b-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="da87b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da87b-106">Parameters</span></span>

 <span data-ttu-id="da87b-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="da87b-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="da87b-108">[out] Una máscara de bits que indica si la carpeta es compatible con el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="da87b-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="da87b-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="da87b-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="da87b-110">Indica que la carpeta no es compatible con el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="da87b-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="da87b-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="da87b-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="da87b-112">Indica que la carpeta es compatible con el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="da87b-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="da87b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da87b-113">Return value</span></span>

<span data-ttu-id="da87b-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="da87b-114">S_OK</span></span> 
  
> <span data-ttu-id="da87b-115">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="da87b-115">The call was successful.</span></span>
    

