---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Última modificación: 20 de febrero de 2012'
ms.openlocfilehash: dd7d310c8e801ba1246a0ce948aced9fa6a1a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818405"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="e5f16-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="e5f16-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="e5f16-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5f16-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5f16-105">Comprueba que un puntero a una cadena de caracteres ancho es válido.</span><span class="sxs-lookup"><span data-stu-id="e5f16-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="e5f16-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5f16-106">Parameters</span></span>

 <span data-ttu-id="e5f16-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="e5f16-107">_lpsz_</span></span>
  
> <span data-ttu-id="e5f16-108">[entrada] Un puntero a la cadena de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="e5f16-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="e5f16-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="e5f16-109">_ucchMax_</span></span>
  
> <span data-ttu-id="e5f16-110">[entrada] La longitud máxima de la cadena de caracteres incluido terminador.</span><span class="sxs-lookup"><span data-stu-id="e5f16-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5f16-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5f16-111">Return value</span></span>

<span data-ttu-id="e5f16-112">Devuelve un valor de tipo Boolean que es true si la cadena es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="e5f16-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5f16-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e5f16-113">Remarks</span></span>

<span data-ttu-id="e5f16-114">Esta función ajusta [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e5f16-114">This function wraps [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="e5f16-115">Para obtener más información, vea [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e5f16-115">For more information, see [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span>
  

