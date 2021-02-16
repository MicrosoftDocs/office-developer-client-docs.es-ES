---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Última modificación: 21 de febrero de 2012'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338468"
---
# <a name="mnls_lstrlenw"></a><span data-ttu-id="c0efb-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="c0efb-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="c0efb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0efb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0efb-105">Determina la longitud de la cadena Unicode especificada, excluyendo el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="c0efb-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="c0efb-106">Considere la posibilidad [de usar StringCchLength en](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) su lugar.</span><span class="sxs-lookup"><span data-stu-id="c0efb-106">Consider using [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="c0efb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0efb-107">Parameters</span></span>

 <span data-ttu-id="c0efb-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="c0efb-108">_lpsz_</span></span>
  
> <span data-ttu-id="c0efb-109">[entrada] Cadena Unicode terminada en null que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="c0efb-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0efb-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0efb-110">Return value</span></span>

<span data-ttu-id="c0efb-111">La función devuelve un entero con la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="c0efb-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="c0efb-112">Es un recuento de caracteres de la cadena, excepto el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="c0efb-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="c0efb-113">Si  _lpsz_ es NULL, la función devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="c0efb-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c0efb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0efb-114">Remarks</span></span>

<span data-ttu-id="c0efb-115">Esta función ajusta la **función lstrlen.**</span><span class="sxs-lookup"><span data-stu-id="c0efb-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="c0efb-116">Para obtener más información, [vea lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c0efb-116">For more information, see [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0efb-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c0efb-117">See also</span></span>



[<span data-ttu-id="c0efb-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="c0efb-118">lstrlen</span></span>](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="c0efb-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="c0efb-119">StringCchLength</span></span>](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

