---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- función initframework [excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34fe8f4a606956b90a0d005b0bc523cea460153f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420758"
---
# <a name="initframework"></a><span data-ttu-id="7966f-104">InitFramework</span><span class="sxs-lookup"><span data-stu-id="7966f-104">InitFramework</span></span>

 <span data-ttu-id="7966f-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7966f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7966f-106">Función de biblioteca de marcos que inicializa la biblioteca de marcos, que simplemente inicializa las estructuras de datos de memoria /  **XLOPER XLOPER12** temporales, liberando cualquier memoria que ya se haya asignado.</span><span class="sxs-lookup"><span data-stu-id="7966f-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="7966f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7966f-107">Parameters</span></span>

<span data-ttu-id="7966f-108">Esta función no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="7966f-108">This function takes no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="7966f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7966f-109">Return value</span></span>

<span data-ttu-id="7966f-110">Esta función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="7966f-110">This function does not return a value.</span></span>
  
## <a name="example"></a><span data-ttu-id="7966f-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7966f-111">Example</span></span>

<span data-ttu-id="7966f-112">En este ejemplo se usa **la función InitFramework** para liberar toda la memoria temporal.</span><span class="sxs-lookup"><span data-stu-id="7966f-112">This example uses the **InitFramework** function to free all temporary memory.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="7966f-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7966f-113">See also</span></span>



[<span data-ttu-id="7966f-114">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="7966f-114">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

