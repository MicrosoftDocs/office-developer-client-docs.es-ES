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
ms.openlocfilehash: 4d3210c098d0a7c83721798c8c32ffd9f1e5ebb4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575465"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="4ef47-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="4ef47-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="4ef47-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ef47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ef47-105">Copia una cadena en un búfer.</span><span class="sxs-lookup"><span data-stu-id="4ef47-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="4ef47-106">No la use.</span><span class="sxs-lookup"><span data-stu-id="4ef47-106">Do not use.</span></span> <span data-ttu-id="4ef47-107">Considere la posibilidad de usar en su lugar [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4ef47-107">Consider using [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="4ef47-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ef47-108">Parameters</span></span>

<span data-ttu-id="4ef47-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="4ef47-109">lpString1</span></span>
  
> <span data-ttu-id="4ef47-110">[out] Un búfer para recibir el contenido de la cadena indicada por el parámetro lpString2.</span><span class="sxs-lookup"><span data-stu-id="4ef47-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="4ef47-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="4ef47-111">lpString2</span></span>
  
> <span data-ttu-id="4ef47-112">[entrada] La cadena terminada en null que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="4ef47-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4ef47-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ef47-113">Return value</span></span>

<span data-ttu-id="4ef47-114">Si la función se realiza correctamente, el valor devuelto es un puntero en el búfer.</span><span class="sxs-lookup"><span data-stu-id="4ef47-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="4ef47-115">Si se produce un error en la función, el valor devuelto es NULL y lpString1 podrían no estar terminada en null.</span><span class="sxs-lookup"><span data-stu-id="4ef47-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ef47-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ef47-116">Remarks</span></span>

<span data-ttu-id="4ef47-117">Esta función ajusta la función **lstrcpy** .</span><span class="sxs-lookup"><span data-stu-id="4ef47-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="4ef47-118">Para obtener más información, vea [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4ef47-118">For more information, see [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4ef47-119">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4ef47-119">See also</span></span>



[<span data-ttu-id="4ef47-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="4ef47-120">lstrcpy</span></span>](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

