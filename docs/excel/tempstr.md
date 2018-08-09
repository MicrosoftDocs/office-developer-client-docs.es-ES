---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- TempStr (función) [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815709"
---
# <a name="tempstr"></a><span data-ttu-id="83de7-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="83de7-104">TempStr</span></span>

 <span data-ttu-id="83de7-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="83de7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="83de7-106">Función de biblioteca Framework en desuso que crea un temporal **XLOPER** que contiene una cadena de bytes **xltypeStr** .</span><span class="sxs-lookup"><span data-stu-id="83de7-106">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string.</span></span> <span data-ttu-id="83de7-107">Toma una cadena terminada en null de origen como entrada.</span><span class="sxs-lookup"><span data-stu-id="83de7-107">It takes a null-terminated source string as input.</span></span> <span data-ttu-id="83de7-108">Intenta sobrescribir el primer carácter de la cadena proporcionada con la longitud de cadena subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="83de7-108">It tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="83de7-109">No siempre es algo seguro: Microsoft Excel podría bloquearse si se pasa una cadena de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="83de7-109">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="83de7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83de7-110">Parameters</span></span>

 <span data-ttu-id="83de7-111">_str_</span><span class="sxs-lookup"><span data-stu-id="83de7-111">_str_</span></span>
  
<span data-ttu-id="83de7-112">Un puntero a la cadena de origen terminada en null.</span><span class="sxs-lookup"><span data-stu-id="83de7-112">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="83de7-113">**TempStr** trunca cadenas que son mayores de 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="83de7-113">**TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="83de7-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83de7-114">Return value</span></span>

<span data-ttu-id="83de7-115">Devuelve una cadena de **xltypeStr** que contiene un puntero en el búfer de cadena que se pasa.</span><span class="sxs-lookup"><span data-stu-id="83de7-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="83de7-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83de7-116">Remarks</span></span>

<span data-ttu-id="83de7-117">Este modo de creación de cadenas temporales ahora está en desuso en favor de la manera en que ambos trabajo [TempStrConst y TempStr12](tempstrconst-tempstr12.md) .</span><span class="sxs-lookup"><span data-stu-id="83de7-117">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work.</span></span> <span data-ttu-id="83de7-118">Estas funciones asignación un nuevo búfer de memoria y copie la cadena que se pasan en él.</span><span class="sxs-lookup"><span data-stu-id="83de7-118">These functions allocate a new memory buffer and copy the passed-in string into it.</span></span> <span data-ttu-id="83de7-119">Las cadenas de entrada para **TempStrConst** y **TempStr12** no se modificarán y por lo que se declaran como **const**.</span><span class="sxs-lookup"><span data-stu-id="83de7-119">The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**.</span></span> <span data-ttu-id="83de7-120">Por el contrario, la cadena de entrada a **TempStr** se ha modificado y no se puede declarar como **const**.</span><span class="sxs-lookup"><span data-stu-id="83de7-120">In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**.</span></span> <span data-ttu-id="83de7-121">El primer carácter de la cadena de entrada se trata como espacio para un carácter de longitud y se sobrescribe por esta función.</span><span class="sxs-lookup"><span data-stu-id="83de7-121">The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="83de7-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="83de7-122">See also</span></span>



[<span data-ttu-id="83de7-123">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="83de7-123">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

