---
title: Referencia de funciones de API de SDK de XLL de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- referencia de la función API [excel 2007], funciones [Excel 2007], referencia [Excel 2007], kit de desarrollo de Software de XLL Excel 2007, referencia
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: e116021a3dc24de7decbe0dad76cc762cd66d032
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715959"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="c6aec-104">Referencia de funciones de API de SDK de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="c6aec-104">Excel XLL SDK API Function Reference</span></span>

<span data-ttu-id="c6aec-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c6aec-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c6aec-106">SDK de XLL de Microsoft Excel 2013 contiene archivos de origen de una biblioteca de marcos diseñados para acelerar la escritura de XLL, además de dos proyectos de ejemplo, Ejemplo y Genérico.</span><span class="sxs-lookup"><span data-stu-id="c6aec-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="c6aec-107">Esta sección proporciona una referencia de función para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c6aec-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="c6aec-108">Devolución de llamadas de Excel a las que puede llamar XLL.</span><span class="sxs-lookup"><span data-stu-id="c6aec-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="c6aec-109">Devolución de llamadas de XLL que busca Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c6aec-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="c6aec-110">Funciones claves de los proyectos de ejemplo y de marco.</span><span class="sxs-lookup"><span data-stu-id="c6aec-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="c6aec-111">Proyectos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6aec-111">Sample projects</span></span>

<span data-ttu-id="c6aec-112">El SDK de XLL de Excel 2013 proporciona archivos de origen y archivos de proyecto de Microsoft Visual Studio para los proyectos de ejemplo siguientes:</span><span class="sxs-lookup"><span data-stu-id="c6aec-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="c6aec-113">El proyecto **Framework** (`SAMPLES\FRAMEWRK\`) contiene un proyecto que puede crearse en una biblioteca, FRAMEWRK.lib, y que, después, puede vincularse a otros proyectos XLL.</span><span class="sxs-lookup"><span data-stu-id="c6aec-113">The **Framework** project (`SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="c6aec-114">La biblioteca contiene muchas funciones y herramientas que facilitan la escritura de XLL.</span><span class="sxs-lookup"><span data-stu-id="c6aec-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="c6aec-115">Esta biblioteca se usa en los otros dos proyectos junto con el archivo de encabezado FRAMEWRK.h.</span><span class="sxs-lookup"><span data-stu-id="c6aec-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="c6aec-116">El proyecto **Example** (`SAMPLES\EXAMPLE\`) contiene un proyecto que puede crearse en un XLL, EXAMPLE.xll.</span><span class="sxs-lookup"><span data-stu-id="c6aec-116">The **Example** project (`SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, EXAMPLE.xll.</span></span> <span data-ttu-id="c6aec-117">El XLL contiene varios ejemplos del uso de la biblioteca de marcos y las implementaciones de ejemplo de las funciones de la interfaz del complemento XLL, como **xlAutoOpen**.</span><span class="sxs-lookup"><span data-stu-id="c6aec-117">The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="c6aec-118">El proyecto **Generic** (`SAMPLES\GENERIC\`) contiene un proyecto que puede crearse en un XLL, GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="c6aec-118">The **Generic** project (`SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="c6aec-119">El XLL muestra varias funciones y comandos de ejemplo y es un buen punto de partida para escribir sus propios XLL.</span><span class="sxs-lookup"><span data-stu-id="c6aec-119">The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="c6aec-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c6aec-120">In this section</span></span>

- [<span data-ttu-id="c6aec-121">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="c6aec-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
- [<span data-ttu-id="c6aec-122">Funciones de devolución de llamada de API de C de Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="c6aec-122">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
- [<span data-ttu-id="c6aec-123">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="c6aec-123">Essential and useful C API XLM functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="c6aec-124">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="c6aec-124">C API functions that can be called only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [<span data-ttu-id="c6aec-125">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="c6aec-125">Functions in the Framework library</span></span>](functions-in-the-framework-library.md)
  
- [<span data-ttu-id="c6aec-126">Funciones en la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="c6aec-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- [<span data-ttu-id="c6aec-127">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="c6aec-127">Excel cluster connector functions</span></span>](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a><span data-ttu-id="c6aec-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6aec-128">See also</span></span>

- [<span data-ttu-id="c6aec-129">Programar con la API de C en Excel</span><span class="sxs-lookup"><span data-stu-id="c6aec-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="c6aec-130">Desarrollo de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="c6aec-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

