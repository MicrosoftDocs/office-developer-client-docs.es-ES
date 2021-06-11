---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- función tempstr [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418046"
---
# <a name="tempstr"></a><span data-ttu-id="282f8-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="282f8-104">TempStr</span></span>

 <span data-ttu-id="282f8-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="282f8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="282f8-106">Función de biblioteca de Framework en desuso que crea un **XLOPER temporal** que contiene una cadena de bytes **xltypeStr.**</span><span class="sxs-lookup"><span data-stu-id="282f8-106">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string.</span></span> <span data-ttu-id="282f8-107">Toma una cadena de origen terminada en null como entrada.</span><span class="sxs-lookup"><span data-stu-id="282f8-107">It takes a null-terminated source string as input.</span></span> <span data-ttu-id="282f8-108">Intenta sobrescribir el primer carácter de la cadena suministrada con la longitud de la cadena posterior.</span><span class="sxs-lookup"><span data-stu-id="282f8-108">It tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="282f8-109">Esto no siempre es algo seguro: Microsoft Excel podría bloquearse si se pasa una cadena de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="282f8-109">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="282f8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="282f8-110">Parameters</span></span>

 <span data-ttu-id="282f8-111">_str_</span><span class="sxs-lookup"><span data-stu-id="282f8-111">_str_</span></span>
  
<span data-ttu-id="282f8-112">Puntero a la cadena de origen terminada en null.</span><span class="sxs-lookup"><span data-stu-id="282f8-112">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="282f8-113">**TempStr** trunca cadenas de más de 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="282f8-113">**TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="282f8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="282f8-114">Return value</span></span>

<span data-ttu-id="282f8-115">Devuelve una **cadena xltypeStr** que contiene un puntero al búfer de cadena pasado.</span><span class="sxs-lookup"><span data-stu-id="282f8-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="282f8-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="282f8-116">Remarks</span></span>

<span data-ttu-id="282f8-117">Esta forma de crear cadenas temporales ahora está en desuso en favor de la forma en que funcionan [TempStrConst y TempStr12.](tempstrconst-tempstr12.md)</span><span class="sxs-lookup"><span data-stu-id="282f8-117">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work.</span></span> <span data-ttu-id="282f8-118">Estas funciones asignan un nuevo búfer de memoria y copian la cadena pasada en él.</span><span class="sxs-lookup"><span data-stu-id="282f8-118">These functions allocate a new memory buffer and copy the passed-in string into it.</span></span> <span data-ttu-id="282f8-119">Las cadenas de entrada **de TempStrConst** y **TempStr12** no se modifican, por lo que se declaran **como const**.</span><span class="sxs-lookup"><span data-stu-id="282f8-119">The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**.</span></span> <span data-ttu-id="282f8-120">En cambio, la cadena de entrada a **TempStr** se modifica y, por lo tanto, no se puede declarar como **const**.</span><span class="sxs-lookup"><span data-stu-id="282f8-120">In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**.</span></span> <span data-ttu-id="282f8-121">El primer carácter de la cadena de entrada se trata como espacio para un carácter de longitud y esta función lo sobrescribe.</span><span class="sxs-lookup"><span data-stu-id="282f8-121">The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="282f8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="282f8-122">See also</span></span>



[<span data-ttu-id="282f8-123">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="282f8-123">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

