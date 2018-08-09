---
title: Funciones de devolución de llamada de API de C de Excel4, Excel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funciones [excel 2007], devolución de llamada de api c
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 221ea4c9c706d11acd31d3f2870d326a7189d299
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815511"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="aa8bf-104">Funciones de devolución de llamada de API de C de Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="aa8bf-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="aa8bf-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="aa8bf-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="aa8bf-106">Las funciones de **Excel4** y **Excel12** se proporcionan para habilitar los DLL en llaman a una función de hoja de cálculo de Microsoft Excel interna, función de hoja de macros o comando, o solo XLL especial o función comando.</span><span class="sxs-lookup"><span data-stu-id="aa8bf-106">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command.</span></span> <span data-ttu-id="aa8bf-107">Todas las versiones recientes de Excel admiten la función de **Excel4** .</span><span class="sxs-lookup"><span data-stu-id="aa8bf-107">All recent versions of Excel support the **Excel4** function.</span></span> <span data-ttu-id="aa8bf-108">Se admite el inicio de la función **Excel12** en Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="aa8bf-108">Starting in Excel 2007 the **Excel12** function is supported.</span></span> <span data-ttu-id="aa8bf-109">Ambas funciones se proporcionan en dos formas:</span><span class="sxs-lookup"><span data-stu-id="aa8bf-109">Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="aa8bf-110">Un formulario de lista de argumentos de longitud variable (**Excel4/Excel12**)</span><span class="sxs-lookup"><span data-stu-id="aa8bf-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="aa8bf-111">Un formulario de matriz de argumentos (**Excel4v/Excel12v**)</span><span class="sxs-lookup"><span data-stu-id="aa8bf-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="aa8bf-112">Salvo en la manera en que los argumentos se pasan a estas devoluciones de llamada, las dos formas son equivalentes funcionalmente.</span><span class="sxs-lookup"><span data-stu-id="aa8bf-112">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent.</span></span> <span data-ttu-id="aa8bf-113">En [Excel4/Excel12](excel4-excel12.md)totalmente se describen los conceptos básicos para las dos formas.</span><span class="sxs-lookup"><span data-stu-id="aa8bf-113">The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md).</span></span> <span data-ttu-id="aa8bf-114">[Excel4v/Excel12v](excel4v-excel12v.md) se describen otros problemas acerca de este formulario.</span><span class="sxs-lookup"><span data-stu-id="aa8bf-114">[Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="aa8bf-115">En esta sección</span><span class="sxs-lookup"><span data-stu-id="aa8bf-115">In this section</span></span>

[<span data-ttu-id="aa8bf-116">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="aa8bf-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="aa8bf-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="aa8bf-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

