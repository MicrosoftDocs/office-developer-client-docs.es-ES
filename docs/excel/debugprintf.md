---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- debugprintf (función) [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815523"
---
# <a name="debugprintf"></a><span data-ttu-id="bc853-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="bc853-104">debugPrintf</span></span>

<span data-ttu-id="bc853-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bc853-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bc853-106">Función de biblioteca de Framework que escribe una cadena de bytes terminada en null en el depurador activo a través de la función de Windows SDK **OutputDebugStringA**.</span><span class="sxs-lookup"><span data-stu-id="bc853-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="bc853-107">Si la aplicación no tiene ningún depurador, el depurador del sistema muestra la cadena.</span><span class="sxs-lookup"><span data-stu-id="bc853-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="bc853-108">Si la aplicación no tiene ningún depurador y el depurador del sistema no está activo, **debugPrintf** no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="bc853-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="bc853-109">Esta función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="bc853-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="bc853-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc853-110">Parameters</span></span>

 <span data-ttu-id="bc853-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="bc853-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="bc853-112">La cadena de formato, que sigue la sintaxis y las reglas para el que se utiliza con la función **sprintf** .</span><span class="sxs-lookup"><span data-stu-id="bc853-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="bc853-113">_argumentos_</span><span class="sxs-lookup"><span data-stu-id="bc853-113">_arguments_</span></span>
  
<span data-ttu-id="bc853-114">Cero o más argumentos para que coincida con la cadena de formato.</span><span class="sxs-lookup"><span data-stu-id="bc853-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="bc853-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc853-115">Example</span></span>

<span data-ttu-id="bc853-116">Esta función imprime una cadena para mostrar que el control se ha pasado a ella.</span><span class="sxs-lookup"><span data-stu-id="bc853-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="bc853-117">El indicador _DEBUG debe definirse antes de compilar, o bien esta función no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="bc853-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a><span data-ttu-id="bc853-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="bc853-118">See also</span></span>



[<span data-ttu-id="bc853-119">Funciones de la biblioteca de Framework</span><span class="sxs-lookup"><span data-stu-id="bc853-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

