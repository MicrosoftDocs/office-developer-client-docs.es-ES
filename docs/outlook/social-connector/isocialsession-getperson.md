---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtiene una interfaz ISocialPerson basándose en el parámetro userID.
ms.openlocfilehash: 5769f4c41bb97f45ab722f1b3a3febe24c8a7ab2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821116"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="6a006-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="6a006-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="6a006-104">Obtiene una interfaz [ISocialPerson](isocialpersoniunknown.md) basándose en el parámetro _userID_ .</span><span class="sxs-lookup"><span data-stu-id="6a006-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="6a006-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a006-105">Parameters</span></span>

<span data-ttu-id="6a006-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="6a006-106">_userId_</span></span>
  
> <span data-ttu-id="6a006-107">[entrada] Una cadena que contiene una dirección SMTP o identificador de usuario de una persona.</span><span class="sxs-lookup"><span data-stu-id="6a006-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="6a006-108">_resultado_</span><span class="sxs-lookup"><span data-stu-id="6a006-108">_result_</span></span>
  
> <span data-ttu-id="6a006-109">[out] Una interfaz **ISocialPerson** .</span><span class="sxs-lookup"><span data-stu-id="6a006-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6a006-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6a006-110">Remarks</span></span>

<span data-ttu-id="6a006-111">El parámetro _userID_ debe ser una dirección SMTP o identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="6a006-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a006-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a006-112">See also</span></span>

- [<span data-ttu-id="6a006-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a006-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

