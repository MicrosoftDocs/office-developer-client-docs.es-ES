---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- initframework (función) [excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2d7e3286d794d6f21da9ef83ca44d18ec242c063
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815633"
---
# <a name="initframework"></a><span data-ttu-id="8d651-104">InitFramework</span><span class="sxs-lookup"><span data-stu-id="8d651-104">InitFramework</span></span>

 <span data-ttu-id="8d651-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8d651-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8d651-106">Función de la biblioteca de Framework que inicializa la biblioteca Framework, que simplemente inicializa el temporal **XLOPER**/ las estructuras de datos de memoria**XLOPER12** , liberar cualquier memoria que ya ha sido asignada.</span><span class="sxs-lookup"><span data-stu-id="8d651-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="8d651-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d651-107">Parameters</span></span>

<span data-ttu-id="8d651-108">Esta función no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="8d651-108">This function takes no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="8d651-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d651-109">Return value</span></span>

<span data-ttu-id="8d651-110">Esta función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="8d651-110">This function does not return a value.</span></span>
  
## <a name="example"></a><span data-ttu-id="8d651-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d651-111">Example</span></span>

<span data-ttu-id="8d651-112">En este ejemplo se usa la función de **InitFramework** para liberar toda la memoria temporal.</span><span class="sxs-lookup"><span data-stu-id="8d651-112">This example uses the **InitFramework** function to free all temporary memory.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="8d651-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d651-113">See also</span></span>



[<span data-ttu-id="8d651-114">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="8d651-114">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

