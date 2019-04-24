---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtiene una interfaz ISocialPerson basada en el parámetro userID.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285333"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="7b790-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="7b790-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="7b790-104">Obtiene una interfaz [ISocialPerson](isocialpersoniunknown.md) basada en el parámetro _userid_ .</span><span class="sxs-lookup"><span data-stu-id="7b790-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="7b790-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="7b790-105">Parameters</span></span>

<span data-ttu-id="7b790-106">_Identificado_</span><span class="sxs-lookup"><span data-stu-id="7b790-106">_userId_</span></span>
  
> <span data-ttu-id="7b790-107">a Una cadena que contiene un identificador de usuario o dirección SMTP de una persona.</span><span class="sxs-lookup"><span data-stu-id="7b790-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="7b790-108">_result_</span><span class="sxs-lookup"><span data-stu-id="7b790-108">_result_</span></span>
  
> <span data-ttu-id="7b790-109">contempla Una interfaz **ISocialPerson** .</span><span class="sxs-lookup"><span data-stu-id="7b790-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7b790-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b790-110">Remarks</span></span>

<span data-ttu-id="7b790-111">El parámetro _userid_ debe ser un identificador de usuario o una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="7b790-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7b790-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b790-112">See also</span></span>

- [<span data-ttu-id="7b790-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b790-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

