---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Last modified: February 20, 2012'
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356857"
---
# <a name="mnls_isbadstringptrw"></a><span data-ttu-id="59744-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="59744-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="59744-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59744-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59744-105">Comprueba que un puntero a una cadena ancha es válido.</span><span class="sxs-lookup"><span data-stu-id="59744-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="59744-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="59744-106">Parameters</span></span>

 <span data-ttu-id="59744-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="59744-107">_lpsz_</span></span>
  
> <span data-ttu-id="59744-108">[in] Puntero a la cadena de caracteres ancho.</span><span class="sxs-lookup"><span data-stu-id="59744-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="59744-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="59744-109">_ucchMax_</span></span>
  
> <span data-ttu-id="59744-110">[in] Longitud máxima de la cadena en caracteres incluido el terminador.</span><span class="sxs-lookup"><span data-stu-id="59744-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="59744-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59744-111">Return value</span></span>

<span data-ttu-id="59744-112">Devuelve un valor Boolean que es true si la cadena es mala.</span><span class="sxs-lookup"><span data-stu-id="59744-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59744-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59744-113">Remarks</span></span>

<span data-ttu-id="59744-114">Esta función ajusta [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="59744-114">This function wraps [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="59744-115">Para obtener más información, [vea IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="59744-115">For more information, see [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span>
  

