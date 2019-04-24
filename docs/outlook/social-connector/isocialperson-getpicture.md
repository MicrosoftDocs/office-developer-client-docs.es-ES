---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Obtiene una matriz de bytes que contiene el recurso de imagen de la persona.
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331657"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="f83b9-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="f83b9-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="f83b9-104">Obtiene una matriz de bytes que contiene el recurso de imagen de la persona.</span><span class="sxs-lookup"><span data-stu-id="f83b9-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="f83b9-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="f83b9-105">Parameters</span></span>

<span data-ttu-id="f83b9-106">_idea_</span><span class="sxs-lookup"><span data-stu-id="f83b9-106">_picture_</span></span>
  
> <span data-ttu-id="f83b9-107">contempla Puntero a una estructura que especifica una matriz de bytes que representa el recurso de imagen de una persona.</span><span class="sxs-lookup"><span data-stu-id="f83b9-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f83b9-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f83b9-108">Remarks</span></span>

<span data-ttu-id="f83b9-109">Los recursos de imagen admitidos están en formato. bmp,. JPEG o. png.</span><span class="sxs-lookup"><span data-stu-id="f83b9-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f83b9-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="f83b9-110">See also</span></span>

- [<span data-ttu-id="f83b9-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f83b9-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

