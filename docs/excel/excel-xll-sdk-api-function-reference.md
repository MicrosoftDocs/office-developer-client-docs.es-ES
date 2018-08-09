---
title: Referencia de funciones de API de SDK de XLL de Excel 2013
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- referencia de la función API [excel 2007], funciones [Excel 2007], referencia [Excel 2007], Kit de desarrollo de Software de XLL de Excel 2007, referencia
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815628"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="a19e0-104">Referencia de funciones de API de SDK de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="a19e0-104">Excel XLL SDK API Function Reference</span></span>

<span data-ttu-id="a19e0-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a19e0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a19e0-106">El SDK de XLL de Microsoft Excel 2013 contiene los archivos de origen para una biblioteca de Framework que está diseñado para acelerar la escritura de los XLL y dos proyectos de ejemplo, ejemplo y genérico.</span><span class="sxs-lookup"><span data-stu-id="a19e0-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="a19e0-107">En esta sección se proporciona una referencia a la función para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a19e0-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="a19e0-108">Las devoluciones de llamada que se puede llamar a los XLL de Excel.</span><span class="sxs-lookup"><span data-stu-id="a19e0-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="a19e0-109">Devoluciones de llamada XLL que busca Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a19e0-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="a19e0-110">Funciones clave en los proyectos de ejemplo y framework.</span><span class="sxs-lookup"><span data-stu-id="a19e0-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="a19e0-111">Proyectos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a19e0-111">Sample projects</span></span>

<span data-ttu-id="a19e0-112">El SDK de XLL de Excel 2013 proporciona archivos de origen y los archivos de proyecto de Microsoft Visual Studio para los proyectos de ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a19e0-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="a19e0-113">El proyecto **Framework** (`SAMPLES\FRAMEWRK\`) contiene un proyecto que puede crearse en una biblioteca, FRAMEWRK.lib, que, a continuación, se pueden vincular a otros proyectos XLL.</span><span class="sxs-lookup"><span data-stu-id="a19e0-113">The **Framework** project (`SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="a19e0-114">La biblioteca contiene muchas funciones y herramientas que hacen que escribir XLL sea más fáciles.</span><span class="sxs-lookup"><span data-stu-id="a19e0-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="a19e0-115">Esta biblioteca se usa en ambos de los otros proyectos junto con el archivo de encabezado FRAMEWRK.h.</span><span class="sxs-lookup"><span data-stu-id="a19e0-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="a19e0-116">El proyecto de **ejemplo** (`SAMPLES\EXAMPLE\`) contiene un proyecto que puede crearse para un XLL, EXAMPLE.xll.</span><span class="sxs-lookup"><span data-stu-id="a19e0-116">The **Example** project (`SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, EXAMPLE.xll.</span></span> <span data-ttu-id="a19e0-117">El XLL contiene muchos ejemplos del uso de la biblioteca de Framework y las implementaciones de ejemplo de las funciones de la interfaz del complemento de XLL como **xlAutoOpen**.</span><span class="sxs-lookup"><span data-stu-id="a19e0-117">The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="a19e0-118">El proyecto **genérico** (`SAMPLES\GENERIC\`) contiene un proyecto que puede crearse para un XLL, GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="a19e0-118">The **Generic** project (`SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="a19e0-119">El XLL muestra varias funciones de ejemplo y los comandos y es un buen punto de partida para escribir su propia XLL.</span><span class="sxs-lookup"><span data-stu-id="a19e0-119">The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="a19e0-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a19e0-120">In this section</span></span>

- [<span data-ttu-id="a19e0-121">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="a19e0-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
- [<span data-ttu-id="a19e0-122">Funciones de devolución de llamada de API de C de Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="a19e0-122">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
- [<span data-ttu-id="a19e0-123">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="a19e0-123">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="a19e0-124">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="a19e0-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [<span data-ttu-id="a19e0-125">Funciones de la biblioteca de marcos</span><span class="sxs-lookup"><span data-stu-id="a19e0-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)
  
- [<span data-ttu-id="a19e0-126">Funciones de la DLL genérica</span><span class="sxs-lookup"><span data-stu-id="a19e0-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- [<span data-ttu-id="a19e0-127">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="a19e0-127">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a><span data-ttu-id="a19e0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a19e0-128">See also</span></span>

- [<span data-ttu-id="a19e0-129">Programar con la API de C en Excel</span><span class="sxs-lookup"><span data-stu-id="a19e0-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="a19e0-130">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="a19e0-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

