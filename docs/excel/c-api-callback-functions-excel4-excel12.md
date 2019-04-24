---
title: Funciones de devolución de llamada de la API de C Excel4, Excel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funciones [Excel 2007], devolución de llamada de la API de c
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5fe5eb7486f12d75ce7e42ad57141480ec735c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304182"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="2ca09-104">Funciones de devolución de llamada de la API de C Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="2ca09-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="2ca09-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2ca09-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2ca09-106">Las funciones de **Excel4** y **Excel12** se proporcionan para habilitar dll para que llame a una función de hoja de cálculo de Microsoft Excel, a una función o a un comando de hoja de macros o a una función o un comando especiales solo XLL.</span><span class="sxs-lookup"><span data-stu-id="2ca09-106">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command.</span></span> <span data-ttu-id="2ca09-107">Todas las versiones recientes de Excel admiten la función **Excel4** .</span><span class="sxs-lookup"><span data-stu-id="2ca09-107">All recent versions of Excel support the **Excel4** function.</span></span> <span data-ttu-id="2ca09-108">A partir de Excel 2007 se admite la función **Excel12** .</span><span class="sxs-lookup"><span data-stu-id="2ca09-108">Starting in Excel 2007 the **Excel12** function is supported.</span></span> <span data-ttu-id="2ca09-109">Ambas funciones se proporcionan en dos formatos:</span><span class="sxs-lookup"><span data-stu-id="2ca09-109">Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="2ca09-110">Un formulario de lista de argumentos de longitud variable (**Excel4/Excel12**)</span><span class="sxs-lookup"><span data-stu-id="2ca09-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="2ca09-111">Una forma de matriz de argumentos (**Excel4v/Excel12v**)</span><span class="sxs-lookup"><span data-stu-id="2ca09-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="2ca09-112">Excepto en la forma en que se pasan los argumentos a estas devoluciones de llamada, los dos formularios son equivalentes funcionalmente.</span><span class="sxs-lookup"><span data-stu-id="2ca09-112">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent.</span></span> <span data-ttu-id="2ca09-113">Los conceptos básicos de ambos formularios se describen completamente en [Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="2ca09-113">The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md).</span></span> <span data-ttu-id="2ca09-114">[Excel4v/Excel12v](excel4v-excel12v.md) cubre otros problemas relacionados con este formulario.</span><span class="sxs-lookup"><span data-stu-id="2ca09-114">[Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="2ca09-115">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2ca09-115">In this section</span></span>

[<span data-ttu-id="2ca09-116">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="2ca09-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="2ca09-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="2ca09-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

