---
title: Funciones de devolución de llamada de la API de C Excel4, Excel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api callback
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5fe5eb7486f12d75ce7e42ad57141480ec735c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434434"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="b1230-104">Funciones de devolución de llamada de la API de C Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="b1230-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="b1230-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b1230-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b1230-106">Las **funciones de Excel4** y **Excel12** se proporcionan para permitir que las DLL llamen Microsoft Excel una función de hoja de cálculo de Microsoft Excel interna, una función o un comando de hoja de macros o un comando especial de solo XLL.</span><span class="sxs-lookup"><span data-stu-id="b1230-106">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command.</span></span> <span data-ttu-id="b1230-107">Todas las versiones recientes de Excel admiten la **función Excel4.**</span><span class="sxs-lookup"><span data-stu-id="b1230-107">All recent versions of Excel support the **Excel4** function.</span></span> <span data-ttu-id="b1230-108">A partir Excel 2007 se admite la función **Excel12.**</span><span class="sxs-lookup"><span data-stu-id="b1230-108">Starting in Excel 2007 the **Excel12** function is supported.</span></span> <span data-ttu-id="b1230-109">Ambas funciones se proporcionan de dos formas:</span><span class="sxs-lookup"><span data-stu-id="b1230-109">Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="b1230-110">Formulario de lista de argumentos de longitud variable (**Excel4/Excel12**)</span><span class="sxs-lookup"><span data-stu-id="b1230-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="b1230-111">Un formulario de matriz de argumentos (**Excel4v/Excel12v**)</span><span class="sxs-lookup"><span data-stu-id="b1230-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="b1230-112">Excepto por la forma en que se pasan los argumentos a estas devoluciones de llamada, los dos formularios son funcionalmente equivalentes.</span><span class="sxs-lookup"><span data-stu-id="b1230-112">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent.</span></span> <span data-ttu-id="b1230-113">Los conceptos básicos de ambos formularios se describen completamente [en Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="b1230-113">The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md).</span></span> <span data-ttu-id="b1230-114">[Excel4v/Excel12v cubre](excel4v-excel12v.md) otros problemas sobre este formulario.</span><span class="sxs-lookup"><span data-stu-id="b1230-114">[Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="b1230-115">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b1230-115">In this section</span></span>

[<span data-ttu-id="b1230-116">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="b1230-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="b1230-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="b1230-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

