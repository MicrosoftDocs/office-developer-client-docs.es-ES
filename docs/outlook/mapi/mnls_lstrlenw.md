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
ms.openlocfilehash: 70c15970ce69e4bc075da6bf55320cb23116b7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818428"
---
# <a name="mnlslstrlenw"></a><span data-ttu-id="cf377-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="cf377-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="cf377-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cf377-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cf377-105">Determina la longitud de la cadena Unicode especificada, excluyendo el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="cf377-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="cf377-106">Considere la posibilidad de usar [StringCchLength](http://msdn.microsoft.com/es-es/library/ms647539%28VS.85%29.aspx) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="cf377-106">Consider using [StringCchLength](http://msdn.microsoft.com/es-es/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="cf377-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf377-107">Parameters</span></span>

 <span data-ttu-id="cf377-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="cf377-108">_lpsz_</span></span>
  
> <span data-ttu-id="cf377-109">[entrada] La cadena Unicode terminada en null que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="cf377-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf377-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf377-110">Return value</span></span>

<span data-ttu-id="cf377-111">La función devuelve un número entero con la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="cf377-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="cf377-112">Es un recuento de caracteres en la cadena, excepto el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="cf377-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="cf377-113">Si _lpsz_ es NULL, la función devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="cf377-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cf377-114">Notas</span><span class="sxs-lookup"><span data-stu-id="cf377-114">Remarks</span></span>

<span data-ttu-id="cf377-115">Esta función ajusta la función **lstrlen** .</span><span class="sxs-lookup"><span data-stu-id="cf377-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="cf377-116">Para obtener más información, vea [lstrlen](http://msdn.microsoft.com/es-es/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cf377-116">For more information, see [lstrlen](http://msdn.microsoft.com/es-es/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf377-117">Ver también</span><span class="sxs-lookup"><span data-stu-id="cf377-117">See also</span></span>



[<span data-ttu-id="cf377-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="cf377-118">lstrlen</span></span>](http://msdn.microsoft.com/es-es/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="cf377-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="cf377-119">StringCchLength</span></span>](http://msdn.microsoft.com/es-es/library/ms647539%28VS.85%29.aspx)

