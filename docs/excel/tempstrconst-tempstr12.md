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
- tempstr12 (función) [excel 2007], TempStrConst (función) [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815712"
---
# <a name="tempstrconsttempstr12"></a><span data-ttu-id="eb31a-104">TempStrConst/TempStr12</span><span class="sxs-lookup"><span data-stu-id="eb31a-104">TempStrConst/TempStr12</span></span>

 <span data-ttu-id="eb31a-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="eb31a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="eb31a-106">Función de la biblioteca de Framework que crea un temporal **XLOPER y XLOPER12** que contiene una cadena **xltypeStr** , tomando una cadena terminada en null de origen como entrada.</span><span class="sxs-lookup"><span data-stu-id="eb31a-106">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input.</span></span> <span data-ttu-id="eb31a-107">La función asigna un nuevo búfer de memoria y copia la cadena que se pasan en él.</span><span class="sxs-lookup"><span data-stu-id="eb31a-107">The function allocates a new memory buffer and copies the passed-in string into it.</span></span> <span data-ttu-id="eb31a-108">La cadena de entrada no se ha modificado y por lo que se declara como **const**.</span><span class="sxs-lookup"><span data-stu-id="eb31a-108">The input string is not altered and so is declared as **const**.</span></span>
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a><span data-ttu-id="eb31a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb31a-109">Parameters</span></span>

 <span data-ttu-id="eb31a-110">_str_</span><span class="sxs-lookup"><span data-stu-id="eb31a-110">_str_</span></span>
  
<span data-ttu-id="eb31a-111">Un puntero a la cadena de origen terminada en null.</span><span class="sxs-lookup"><span data-stu-id="eb31a-111">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="eb31a-112">En el caso de s **XLOPER**, TempStrConst trunca cadenas que son mayores de 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="eb31a-112">In the case of **XLOPER**s, TempStrConst truncates strings that are longer than 255 bytes.</span></span> <span data-ttu-id="eb31a-113">En el caso de s **XLOPER12**, TempStr12Const trunca cadenas que son más de 32.767 caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="eb31a-113">In the case of **XLOPER12**s, TempStr12Const truncates strings that are longer than 32,767 Unicode characters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="eb31a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb31a-114">Return value</span></span>

<span data-ttu-id="eb31a-115">Devuelve una cadena de **xltypeStr** que contiene una copia del búfer se pasan en la cadena.</span><span class="sxs-lookup"><span data-stu-id="eb31a-115">Returns an **xltypeStr** string containing a copy of the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="eb31a-116">Notas</span><span class="sxs-lookup"><span data-stu-id="eb31a-116">Remarks</span></span>

<span data-ttu-id="eb31a-117">Tenga en cuenta que la cadena **XLOPER** función Framework, **TempStr**, se comporta de manera diferente e intenta sobrescribir el primer carácter de la cadena proporcionada con la longitud de cadena subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="eb31a-117">Note that the **XLOPER** string Framework function, **TempStr**, behaves differently and tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="eb31a-118">No siempre es algo seguro: Microsoft Excel podría bloquearse si se pasa una cadena de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="eb31a-118">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> <span data-ttu-id="eb31a-119">Este modo de creación de cadenas temporales ahora está en desuso en favor de la manera en que trabajan **TempStrConst** y **TempStr12** .</span><span class="sxs-lookup"><span data-stu-id="eb31a-119">This way of creating temporary strings is now deprecated in favor of the way in which both **TempStrConst** and **TempStr12** work.</span></span> <span data-ttu-id="eb31a-120">Por lo tanto, el primer carácter de la cadena de entrada se trata como el inicio de la cadena, es decir, no como un carácter de longitud o como un espacio para un carácter de longitud.</span><span class="sxs-lookup"><span data-stu-id="eb31a-120">Therefore the first character of the input string is treated as the start of the string, that is, not as a length character or as a space for a length character.</span></span> <span data-ttu-id="eb31a-121">No debe pasar las cadenas que tienen un carácter de longitud codificado al principio, como las consecuencias podrían ser impredecibles.</span><span class="sxs-lookup"><span data-stu-id="eb31a-121">You should not pass strings that have a length character encoded at the start, as the consequences could be unpredictable.</span></span> 
  
## <a name="example"></a><span data-ttu-id="eb31a-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb31a-122">Example</span></span>

<span data-ttu-id="eb31a-123">En este ejemplo se usa la función **TempStr12** para crear una cadena de un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="eb31a-123">This example uses the **TempStr12** function to create a string for a message box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="eb31a-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="eb31a-124">See also</span></span>



[<span data-ttu-id="eb31a-125">Funciones de la biblioteca de Framework</span><span class="sxs-lookup"><span data-stu-id="eb31a-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

