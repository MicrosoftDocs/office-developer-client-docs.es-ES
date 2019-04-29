---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- función debugprintf [Excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424801"
---
# <a name="debugprintf"></a><span data-ttu-id="f666f-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="f666f-104">debugPrintf</span></span>

<span data-ttu-id="f666f-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f666f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f666f-106">Función de biblioteca de .NET Framework que escribe una cadena de bytes terminada en null en el depurador activo a través de la función **OutputDebugStringA**de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f666f-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="f666f-107">Si la aplicación no tiene depurador, el depurador del sistema muestra la cadena.</span><span class="sxs-lookup"><span data-stu-id="f666f-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="f666f-108">Si la aplicación no tiene ningún depurador y el depurador del sistema no está activo, **debugPrintf** no realiza ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="f666f-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="f666f-109">Esta función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="f666f-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="f666f-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="f666f-110">Parameters</span></span>

 <span data-ttu-id="f666f-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="f666f-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="f666f-112">La cadena de formato, que sigue a la sintaxis y las reglas que se usan con la función **sprintf** .</span><span class="sxs-lookup"><span data-stu-id="f666f-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="f666f-113">_argumentos_</span><span class="sxs-lookup"><span data-stu-id="f666f-113">_arguments_</span></span>
  
<span data-ttu-id="f666f-114">Cero o más argumentos para coincidir con la cadena de formato.</span><span class="sxs-lookup"><span data-stu-id="f666f-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="f666f-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f666f-115">Example</span></span>

<span data-ttu-id="f666f-116">Esta función imprime una cadena para mostrar que se ha pasado el control.</span><span class="sxs-lookup"><span data-stu-id="f666f-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="f666f-117">La marca _ Debug debe definirse antes de compilar o, de lo contrario, esta función no realiza ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="f666f-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="f666f-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="f666f-118">See also</span></span>



[<span data-ttu-id="f666f-119">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="f666f-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

