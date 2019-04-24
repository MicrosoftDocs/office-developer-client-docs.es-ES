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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341730"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="2317e-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="2317e-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="2317e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2317e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2317e-105">Copia una cadena en un búfer.</span><span class="sxs-lookup"><span data-stu-id="2317e-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="2317e-106">No usar.</span><span class="sxs-lookup"><span data-stu-id="2317e-106">Do not use.</span></span> <span data-ttu-id="2317e-107">Considere la posibilidad de usar [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="2317e-107">Consider using [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="2317e-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="2317e-108">Parameters</span></span>

<span data-ttu-id="2317e-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="2317e-109">lpString1</span></span>
  
> <span data-ttu-id="2317e-110">contempla Un búfer para recibir el contenido de la cadena a la que señala el parámetro lpString2.</span><span class="sxs-lookup"><span data-stu-id="2317e-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="2317e-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="2317e-111">lpString2</span></span>
  
> <span data-ttu-id="2317e-112">a Cadena terminada en null que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="2317e-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2317e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2317e-113">Return value</span></span>

<span data-ttu-id="2317e-114">Si la función se ejecuta correctamente, el valor devuelto es un puntero al búfer.</span><span class="sxs-lookup"><span data-stu-id="2317e-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="2317e-115">Si se produce un error en la función, el valor devuelto es NULL y lpString1 no puede terminar en NULL.</span><span class="sxs-lookup"><span data-stu-id="2317e-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2317e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2317e-116">Remarks</span></span>

<span data-ttu-id="2317e-117">Esta función ajusta la función **lstrcpy** .</span><span class="sxs-lookup"><span data-stu-id="2317e-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="2317e-118">Para obtener más información, vea [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2317e-118">For more information, see [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2317e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2317e-119">See also</span></span>



[<span data-ttu-id="2317e-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="2317e-120">lstrcpy</span></span>](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

