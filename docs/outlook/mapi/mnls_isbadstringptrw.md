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
ms.openlocfilehash: 0052d0bd6b485340a92cca9f22ca65c9e2442df6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589570"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="84f79-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="84f79-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="84f79-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84f79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84f79-105">Comprueba que un puntero a una cadena de caracteres ancho es válido.</span><span class="sxs-lookup"><span data-stu-id="84f79-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="84f79-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84f79-106">Parameters</span></span>

 <span data-ttu-id="84f79-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="84f79-107">_lpsz_</span></span>
  
> <span data-ttu-id="84f79-108">[entrada] Un puntero a la cadena de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="84f79-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="84f79-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="84f79-109">_ucchMax_</span></span>
  
> <span data-ttu-id="84f79-110">[entrada] La longitud máxima de la cadena de caracteres incluido terminador.</span><span class="sxs-lookup"><span data-stu-id="84f79-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84f79-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84f79-111">Return value</span></span>

<span data-ttu-id="84f79-112">Devuelve un valor de tipo Boolean que es true si la cadena es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="84f79-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="84f79-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84f79-113">Remarks</span></span>

<span data-ttu-id="84f79-114">Esta función ajusta [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="84f79-114">This function wraps [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="84f79-115">Para obtener más información, vea [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="84f79-115">For more information, see [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span>
  

