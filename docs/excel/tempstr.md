---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- función tempstr [Excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310321"
---
# <a name="tempstr"></a><span data-ttu-id="45700-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="45700-104">TempStr</span></span>

 <span data-ttu-id="45700-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="45700-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="45700-106">Función de biblioteca de Framework en desuso que crea un **XLOPER** temporal que contiene una cadena de bytes **xltypeStr** .</span><span class="sxs-lookup"><span data-stu-id="45700-106">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string.</span></span> <span data-ttu-id="45700-107">Toma una cadena de origen terminada en NULL como entrada.</span><span class="sxs-lookup"><span data-stu-id="45700-107">It takes a null-terminated source string as input.</span></span> <span data-ttu-id="45700-108">Intenta sobrescribir el primer carácter de la cadena proporcionada con la longitud de la cadena subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="45700-108">It tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="45700-109">No siempre es un aspecto seguro que hacer: Microsoft Excel puede bloquearse si se pasa una cadena de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="45700-109">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="45700-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45700-110">Parameters</span></span>

 <span data-ttu-id="45700-111">_str_</span><span class="sxs-lookup"><span data-stu-id="45700-111">_str_</span></span>
  
<span data-ttu-id="45700-112">Un puntero a la cadena de origen terminada en nulo.</span><span class="sxs-lookup"><span data-stu-id="45700-112">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="45700-113">**TempStr** trunca las cadenas que tienen más de 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="45700-113">**TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="45700-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45700-114">Return value</span></span>

<span data-ttu-id="45700-115">Devuelve una cadena **xltypeStr** que contiene un puntero al búfer de cadena pasado.</span><span class="sxs-lookup"><span data-stu-id="45700-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="45700-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="45700-116">Remarks</span></span>

<span data-ttu-id="45700-117">Esta manera de crear cadenas temporales ahora está en desuso en favor de la forma en que funcionan tanto [TempStrConst como TempStr12](tempstrconst-tempstr12.md) .</span><span class="sxs-lookup"><span data-stu-id="45700-117">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work.</span></span> <span data-ttu-id="45700-118">Estas funciones asignan un nuevo búfer de memoria y copian la cadena que se ha pasado en ella.</span><span class="sxs-lookup"><span data-stu-id="45700-118">These functions allocate a new memory buffer and copy the passed-in string into it.</span></span> <span data-ttu-id="45700-119">No se modifican las cadenas de entrada de **TempStrConst** y **TempStr12** , por lo que se declaran como **const**.</span><span class="sxs-lookup"><span data-stu-id="45700-119">The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**.</span></span> <span data-ttu-id="45700-120">Por el contrario, se modifica la cadena de entrada a **TempStr** y, por lo tanto, no se puede declarar como **const**.</span><span class="sxs-lookup"><span data-stu-id="45700-120">In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**.</span></span> <span data-ttu-id="45700-121">El primer carácter de la cadena de entrada se trata como espacio para un carácter de longitud y se sobrescribe con esta función.</span><span class="sxs-lookup"><span data-stu-id="45700-121">The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="45700-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="45700-122">See also</span></span>



[<span data-ttu-id="45700-123">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="45700-123">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

