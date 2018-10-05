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
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398741"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="31af6-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="31af6-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="31af6-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31af6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31af6-105">Comprueba que un puntero a una cadena de caracteres ancho es válido.</span><span class="sxs-lookup"><span data-stu-id="31af6-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="31af6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31af6-106">Parameters</span></span>

 <span data-ttu-id="31af6-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="31af6-107">_lpsz_</span></span>
  
> <span data-ttu-id="31af6-108">[entrada] Un puntero a la cadena de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="31af6-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="31af6-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="31af6-109">_ucchMax_</span></span>
  
> <span data-ttu-id="31af6-110">[entrada] La longitud máxima de la cadena de caracteres incluido terminador.</span><span class="sxs-lookup"><span data-stu-id="31af6-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31af6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31af6-111">Return value</span></span>

<span data-ttu-id="31af6-112">Devuelve un valor de tipo Boolean que es true si la cadena es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="31af6-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31af6-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31af6-113">Remarks</span></span>

<span data-ttu-id="31af6-114">Esta función ajusta [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="31af6-114">This function wraps [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="31af6-115">Para obtener más información, vea [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="31af6-115">For more information, see [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span>
  

