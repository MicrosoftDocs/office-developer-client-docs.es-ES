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
- función tempmissing [excel 2007],Función TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 37c127b2252f18643b34dfc72fd9929885a68d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435960"
---
# <a name="tempmissingtempmissing12"></a><span data-ttu-id="34108-104">TempMissing/TempMissing12</span><span class="sxs-lookup"><span data-stu-id="34108-104">TempMissing/TempMissing12</span></span>

 <span data-ttu-id="34108-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="34108-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="34108-106">Función de biblioteca de marcos que crea un **XLOPER** /  **XLOPER12** temporal de tipo **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="34108-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** of type **xltypeMissing**.</span></span>
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a><span data-ttu-id="34108-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34108-107">Parameters</span></span>

<span data-ttu-id="34108-108">Esta función no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="34108-108">This function takes no parameters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="34108-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34108-109">Return value</span></span>

<span data-ttu-id="34108-110">Devuelve un puntero a **un xltypeMissing** **XLOPER** /  **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="34108-110">Returns a pointer to an **xltypeMissing** **XLOPER**/ **XLOPER12**.</span></span>
  
## <a name="example"></a><span data-ttu-id="34108-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34108-111">Example</span></span>

<span data-ttu-id="34108-112">En este ejemplo se **usa TempMissing12** para proporcionar tres argumentos que faltan a **xlcWorkspace** seguidos de **un valor** **FALSE** booleano para suprimir la presentación de las barras de desplazamiento de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="34108-112">This example uses **TempMissing12** to provide three missing arguments to **xlcWorkspace** followed by a **Boolean** **FALSE** to suppress the display of worksheet scroll bars.</span></span> <span data-ttu-id="34108-113">Los tres primeros argumentos corresponden a otras configuraciones de área de trabajo que no se ven afectadas.</span><span class="sxs-lookup"><span data-stu-id="34108-113">The first three arguments correspond to other workspace settings which are unaffected.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="34108-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="34108-114">See also</span></span>



[<span data-ttu-id="34108-115">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="34108-115">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

