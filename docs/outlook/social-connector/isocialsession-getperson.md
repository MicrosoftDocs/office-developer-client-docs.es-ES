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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439824"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="c30d2-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="c30d2-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="c30d2-104">Obtiene una [interfaz ISocialPerson](isocialpersoniunknown.md) basada en el _parámetro userID._</span><span class="sxs-lookup"><span data-stu-id="c30d2-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="c30d2-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c30d2-105">Parameters</span></span>

<span data-ttu-id="c30d2-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="c30d2-106">_userId_</span></span>
  
> <span data-ttu-id="c30d2-107">[entrada] Cadena que contiene un identificador de usuario o una dirección SMTP de una persona.</span><span class="sxs-lookup"><span data-stu-id="c30d2-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="c30d2-108">_result_</span><span class="sxs-lookup"><span data-stu-id="c30d2-108">_result_</span></span>
  
> <span data-ttu-id="c30d2-109">[salida] Una **interfaz ISocialPerson.**</span><span class="sxs-lookup"><span data-stu-id="c30d2-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c30d2-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c30d2-110">Remarks</span></span>

<span data-ttu-id="c30d2-111">El  _parámetro userID_ debe ser un identificador de usuario o una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="c30d2-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c30d2-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c30d2-112">See also</span></span>

- [<span data-ttu-id="c30d2-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c30d2-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

