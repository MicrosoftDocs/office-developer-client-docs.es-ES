---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Obtiene una matriz de bytes que contiene el recurso de imagen para la persona.
ms.openlocfilehash: dcb0da5bc36c2166d569c770d1f182cd21339435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821095"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="d789d-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="d789d-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="d789d-104">Obtiene una matriz de bytes que contiene el recurso de imagen para la persona.</span><span class="sxs-lookup"><span data-stu-id="d789d-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="d789d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d789d-105">Parameters</span></span>

<span data-ttu-id="d789d-106">_imagen_</span><span class="sxs-lookup"><span data-stu-id="d789d-106">_picture_</span></span>
  
> <span data-ttu-id="d789d-107">[out] Un puntero a una estructura que especifica una matriz de bytes que representan el recurso de imagen de una persona.</span><span class="sxs-lookup"><span data-stu-id="d789d-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d789d-108">Notas</span><span class="sxs-lookup"><span data-stu-id="d789d-108">Remarks</span></span>

<span data-ttu-id="d789d-109">Compatible con los recursos están en .bmp, .jpeg o .png formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="d789d-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d789d-110">Ver también</span><span class="sxs-lookup"><span data-stu-id="d789d-110">See also</span></span>

- [<span data-ttu-id="d789d-111">ISocialPerson: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d789d-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

