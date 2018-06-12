---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- tempmissing (función) [excel 2007], TempMissing12 (función) [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815707"
---
# <a name="tempmissingtempmissing12"></a><span data-ttu-id="718a6-104">TempMissing/TempMissing12</span><span class="sxs-lookup"><span data-stu-id="718a6-104">TempMissing/TempMissing12</span></span>

 <span data-ttu-id="718a6-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="718a6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="718a6-106">Función de la biblioteca de Framework que crea un temporal **XLOPER**/ **XLOPER12** de tipo **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="718a6-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** of type **xltypeMissing**.</span></span>
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a><span data-ttu-id="718a6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="718a6-107">Parameters</span></span>

<span data-ttu-id="718a6-108">Esta función no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="718a6-108">This function takes no parameters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="718a6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="718a6-109">Return value</span></span>

<span data-ttu-id="718a6-110">Devuelve un puntero a un **xltypeMissing** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="718a6-110">Returns a pointer to an **xltypeMissing** **XLOPER**/ **XLOPER12**.</span></span>
  
## <a name="example"></a><span data-ttu-id="718a6-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="718a6-111">Example</span></span>

<span data-ttu-id="718a6-112">En este ejemplo se utiliza **TempMissing12** para proporcionar tres argumentos que faltan a **xlcWorkspace** seguido de un **valor Boolean** **FALSE** para suprimir la presentación de las barras de desplazamiento de hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="718a6-112">This example uses **TempMissing12** to provide three missing arguments to **xlcWorkspace** followed by a **Boolean** **FALSE** to suppress the display of worksheet scroll bars.</span></span> <span data-ttu-id="718a6-113">Los tres primeros argumentos corresponden a otras opciones de área de trabajo que no se ven afectados.</span><span class="sxs-lookup"><span data-stu-id="718a6-113">The first three arguments correspond to other workspace settings which are unaffected.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="718a6-114">Ver también</span><span class="sxs-lookup"><span data-stu-id="718a6-114">See also</span></span>



[<span data-ttu-id="718a6-115">Funciones de la biblioteca de Framework</span><span class="sxs-lookup"><span data-stu-id="718a6-115">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

