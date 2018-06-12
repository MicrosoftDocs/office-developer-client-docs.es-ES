---
title: IMAPIFormInfoOpenFormContainer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.OpenFormContainer
api_type:
- COM
ms.assetid: 1d6eec99-59f9-4700-9b83-7f7f8787a9f8
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: f6461a1e47437c5d0c2c422d727e2b00819629b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817290"
---
# <a name="imapiforminfoopenformcontainer"></a><span data-ttu-id="76556-103">IMAPIFormInfo::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="76556-103">IMAPIFormInfo::OpenFormContainer</span></span>

  
  
<span data-ttu-id="76556-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76556-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76556-105">Devuelve un puntero al contenedor de formulario en el que está instalado un formulario en particular.</span><span class="sxs-lookup"><span data-stu-id="76556-105">Returns a pointer to the form container in which a particular form is installed.</span></span>
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a><span data-ttu-id="76556-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76556-106">Parameters</span></span>

 <span data-ttu-id="76556-107">_ppformcontainer_</span><span class="sxs-lookup"><span data-stu-id="76556-107">_ppformcontainer_</span></span>
  
> <span data-ttu-id="76556-108">[out] Un puntero a un puntero al objeto de contenedor de formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="76556-108">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="76556-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76556-109">Return value</span></span>

<span data-ttu-id="76556-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="76556-110">S_OK</span></span> 
  
> <span data-ttu-id="76556-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="76556-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76556-112">Ver también</span><span class="sxs-lookup"><span data-stu-id="76556-112">See also</span></span>



[<span data-ttu-id="76556-113">IMAPIFormInfo: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="76556-113">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

