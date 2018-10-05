---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Última modificación: 18 de junio de 2012'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382711"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="18170-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="18170-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="18170-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18170-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18170-105">Copia una cadena en un búfer.</span><span class="sxs-lookup"><span data-stu-id="18170-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="18170-106">No la use.</span><span class="sxs-lookup"><span data-stu-id="18170-106">Do not use.</span></span> <span data-ttu-id="18170-107">Considere la posibilidad de usar en su lugar [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="18170-107">Consider using [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="18170-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18170-108">Parameters</span></span>

<span data-ttu-id="18170-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="18170-109">lpString1</span></span>
  
> <span data-ttu-id="18170-110">[out] Un búfer para recibir el contenido de la cadena indicada por el parámetro lpString2.</span><span class="sxs-lookup"><span data-stu-id="18170-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="18170-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="18170-111">lpString2</span></span>
  
> <span data-ttu-id="18170-112">[entrada] La cadena terminada en null que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="18170-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="18170-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18170-113">Return value</span></span>

<span data-ttu-id="18170-114">Si la función se realiza correctamente, el valor devuelto es un puntero en el búfer.</span><span class="sxs-lookup"><span data-stu-id="18170-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="18170-115">Si se produce un error en la función, el valor devuelto es NULL y lpString1 podrían no estar terminada en null.</span><span class="sxs-lookup"><span data-stu-id="18170-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18170-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18170-116">Remarks</span></span>

<span data-ttu-id="18170-117">Esta función ajusta la función **lstrcpy** .</span><span class="sxs-lookup"><span data-stu-id="18170-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="18170-118">Para obtener más información, vea [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="18170-118">For more information, see [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18170-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="18170-119">See also</span></span>



[<span data-ttu-id="18170-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="18170-120">lstrcpy</span></span>](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

