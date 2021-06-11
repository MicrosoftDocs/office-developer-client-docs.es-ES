---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- función tempstr12 [excel 2007],Función TempStrConst [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d93f9de021c7ba325d9c11af2cede0245ffbbf6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407154"
---
# <a name="tempstrconsttempstr12"></a><span data-ttu-id="045a2-104">TempStrConst/TempStr12</span><span class="sxs-lookup"><span data-stu-id="045a2-104">TempStrConst/TempStr12</span></span>

 <span data-ttu-id="045a2-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="045a2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="045a2-106">Función de biblioteca de marcos que crea una **XLOPER/XLOPER12** temporal que contiene una cadena **xltypeStr,** tomando una cadena de origen terminada en null como entrada.</span><span class="sxs-lookup"><span data-stu-id="045a2-106">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input.</span></span> <span data-ttu-id="045a2-107">La función asigna un nuevo búfer de memoria y copia la cadena pasada en él.</span><span class="sxs-lookup"><span data-stu-id="045a2-107">The function allocates a new memory buffer and copies the passed-in string into it.</span></span> <span data-ttu-id="045a2-108">La cadena de entrada no se modifica y, por lo tanto, se declara **como const**.</span><span class="sxs-lookup"><span data-stu-id="045a2-108">The input string is not altered and so is declared as **const**.</span></span>
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a><span data-ttu-id="045a2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="045a2-109">Parameters</span></span>

 <span data-ttu-id="045a2-110">_str_</span><span class="sxs-lookup"><span data-stu-id="045a2-110">_str_</span></span>
  
<span data-ttu-id="045a2-111">Puntero a la cadena de origen terminada en null.</span><span class="sxs-lookup"><span data-stu-id="045a2-111">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="045a2-112">En el caso de **XLOPER** s, TempStrConst trunca cadenas de más de 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="045a2-112">In the case of **XLOPER** s, TempStrConst truncates strings that are longer than 255 bytes.</span></span> <span data-ttu-id="045a2-113">En el caso de **XLOPER12** s, TempStr12Const trunca cadenas que tienen más de 32.767 caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="045a2-113">In the case of **XLOPER12** s, TempStr12Const truncates strings that are longer than 32,767 Unicode characters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="045a2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="045a2-114">Return value</span></span>

<span data-ttu-id="045a2-115">Devuelve una **cadena xltypeStr** que contiene una copia del búfer de cadena pasado.</span><span class="sxs-lookup"><span data-stu-id="045a2-115">Returns an **xltypeStr** string containing a copy of the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="045a2-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="045a2-116">Remarks</span></span>

<span data-ttu-id="045a2-117">Tenga en cuenta que la función Marco de cadena **XLOPER,** **TempStr**, se comporta de forma diferente e intenta sobrescribir el primer carácter de la cadena suministrada con la longitud de la cadena posterior.</span><span class="sxs-lookup"><span data-stu-id="045a2-117">Note that the **XLOPER** string Framework function, **TempStr**, behaves differently and tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="045a2-118">Esto no siempre es algo seguro: Microsoft Excel podría bloquearse si se pasa una cadena de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="045a2-118">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> <span data-ttu-id="045a2-119">Esta forma de crear cadenas temporales ahora está en desuso en favor de la forma en que funcionan **TempStrConst** y **TempStr12.**</span><span class="sxs-lookup"><span data-stu-id="045a2-119">This way of creating temporary strings is now deprecated in favor of the way in which both **TempStrConst** and **TempStr12** work.</span></span> <span data-ttu-id="045a2-120">Por lo tanto, el primer carácter de la cadena de entrada se trata como el inicio de la cadena, es decir, no como un carácter de longitud o como un espacio para un carácter de longitud.</span><span class="sxs-lookup"><span data-stu-id="045a2-120">Therefore the first character of the input string is treated as the start of the string, that is, not as a length character or as a space for a length character.</span></span> <span data-ttu-id="045a2-121">No debe pasar cadenas que tengan un carácter de longitud codificado al principio, ya que las consecuencias podrían ser impredecibles.</span><span class="sxs-lookup"><span data-stu-id="045a2-121">You should not pass strings that have a length character encoded at the start, as the consequences could be unpredictable.</span></span> 
  
## <a name="example"></a><span data-ttu-id="045a2-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="045a2-122">Example</span></span>

<span data-ttu-id="045a2-123">En este ejemplo se usa **la función TempStr12** para crear una cadena para un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="045a2-123">This example uses the **TempStr12** function to create a string for a message box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="045a2-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="045a2-124">See also</span></span>



[<span data-ttu-id="045a2-125">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="045a2-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

