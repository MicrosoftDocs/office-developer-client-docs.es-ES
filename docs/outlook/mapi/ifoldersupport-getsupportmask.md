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
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417374"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="9bb7b-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="9bb7b-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="9bb7b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bb7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bb7b-105">Obtiene información sobre la compatibilidad de una carpeta para compartir.</span><span class="sxs-lookup"><span data-stu-id="9bb7b-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="9bb7b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9bb7b-106">Parameters</span></span>

 <span data-ttu-id="9bb7b-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="9bb7b-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="9bb7b-108">[salida] Máscara de bits que indica si la carpeta admite el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="9bb7b-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="9bb7b-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="9bb7b-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="9bb7b-110">Indica que la carpeta no admite el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="9bb7b-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="9bb7b-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="9bb7b-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="9bb7b-112">Indica que la carpeta admite el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="9bb7b-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9bb7b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9bb7b-113">Return value</span></span>

<span data-ttu-id="9bb7b-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="9bb7b-114">S_OK</span></span> 
  
> <span data-ttu-id="9bb7b-115">La llamada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9bb7b-115">The call was successful.</span></span>
    

