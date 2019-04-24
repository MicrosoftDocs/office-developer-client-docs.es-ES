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
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a76d0c554d7cf06aceeaa2925c199e45411b999d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342094"
---
# <a name="imapiforminfoopenformcontainer"></a><span data-ttu-id="471f0-103">IMAPIFormInfo::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="471f0-103">IMAPIFormInfo::OpenFormContainer</span></span>

  
  
<span data-ttu-id="471f0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="471f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="471f0-105">Devuelve un puntero al contenedor de formularios en el que se instala un formulario determinado.</span><span class="sxs-lookup"><span data-stu-id="471f0-105">Returns a pointer to the form container in which a particular form is installed.</span></span>
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a><span data-ttu-id="471f0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="471f0-106">Parameters</span></span>

 <span data-ttu-id="471f0-107">_ppformcontainer_</span><span class="sxs-lookup"><span data-stu-id="471f0-107">_ppformcontainer_</span></span>
  
> <span data-ttu-id="471f0-108">contempla Un puntero a un puntero al objeto de contenedor de formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="471f0-108">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="471f0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="471f0-109">Return value</span></span>

<span data-ttu-id="471f0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="471f0-110">S_OK</span></span> 
  
> <span data-ttu-id="471f0-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="471f0-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="471f0-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="471f0-112">See also</span></span>



[<span data-ttu-id="471f0-113">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="471f0-113">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

