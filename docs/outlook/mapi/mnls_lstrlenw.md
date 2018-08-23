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
ms.openlocfilehash: 1135a8e07bf94a200d06db8b692ee39dfdb78272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588891"
---
# <a name="mnlslstrlenw"></a><span data-ttu-id="106d4-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="106d4-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="106d4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="106d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="106d4-105">Determina la longitud de la cadena Unicode especificada, excluyendo el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="106d4-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="106d4-106">Considere la posibilidad de usar [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="106d4-106">Consider using [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="106d4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="106d4-107">Parameters</span></span>

 <span data-ttu-id="106d4-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="106d4-108">_lpsz_</span></span>
  
> <span data-ttu-id="106d4-109">[entrada] La cadena Unicode terminada en null que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="106d4-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="106d4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="106d4-110">Return value</span></span>

<span data-ttu-id="106d4-111">La función devuelve un número entero con la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="106d4-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="106d4-112">Es un recuento de caracteres en la cadena, excepto el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="106d4-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="106d4-113">Si _lpsz_ es NULL, la función devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="106d4-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="106d4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="106d4-114">Remarks</span></span>

<span data-ttu-id="106d4-115">Esta función ajusta la función **lstrlen** .</span><span class="sxs-lookup"><span data-stu-id="106d4-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="106d4-116">Para obtener más información, vea [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="106d4-116">For more information, see [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="106d4-117">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="106d4-117">See also</span></span>



[<span data-ttu-id="106d4-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="106d4-118">lstrlen</span></span>](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="106d4-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="106d4-119">StringCchLength</span></span>](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)

