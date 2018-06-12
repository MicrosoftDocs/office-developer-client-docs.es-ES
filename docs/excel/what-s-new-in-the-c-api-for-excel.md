---
title: Novedades de la API C para Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api de c [excel 2007], novedades
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815702"
---
# <a name="whats-new-in-the-c-api-for-excel"></a><span data-ttu-id="96a73-104">Novedades de la API C para Excel</span><span class="sxs-lookup"><span data-stu-id="96a73-104">What's New in the C API for Excel</span></span>

 <span data-ttu-id="96a73-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="96a73-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="96a73-106">Junto con Microsoft Excel 2013, el Kit de desarrollo de Software (SDK) de Microsoft Excel 2013 XLL incluye compatibilidad con las siguientes características.</span><span class="sxs-lookup"><span data-stu-id="96a73-106">In conjunction with Microsoft Excel 2013, the Microsoft Excel 2013 XLL Software Development Kit (SDK) includes support for the following features.</span></span>
  
- <span data-ttu-id="96a73-107">**Nuevas funciones**</span><span class="sxs-lookup"><span data-stu-id="96a73-107">**New Functions**</span></span>
    
    <span data-ttu-id="96a73-108">El SDK de XLL de Microsoft Excel 2013 admite la devolución de llamada para todas las nuevas funciones de hoja de cálculo en Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="96a73-108">The Microsoft Excel 2013 XLL SDK supports calling back to all of the new worksheet functions in Excel 2013.</span></span> <span data-ttu-id="96a73-109">Para obtener más información sobre cómo llamar a funciones de Excel 2013, consulte [Calling a Excel desde el archivo DLL o XLL](calling-into-excel-from-the-dll-or-xll.md).</span><span class="sxs-lookup"><span data-stu-id="96a73-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span></span>
    
- <span data-ttu-id="96a73-110">**Funciones asincrónicas definidas por el usuario**</span><span class="sxs-lookup"><span data-stu-id="96a73-110">**Asynchronous User-defined Functions**</span></span>
    
    <span data-ttu-id="96a73-111">Excel 2013 admite llamar a funciones definidas por el usuario (UDF) de forma asincrónica, que puede mejorar el rendimiento mediante la habilitación de varios cálculos ejecutar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="96a73-111">Excel 2013 supports calling user-defined functions (UDF) asynchronously, which can improve performance by enabling several calculations to run at the same time.</span></span> <span data-ttu-id="96a73-112">Para obtener más información acerca de las UDF asincrónicas, vea [Funciones de Asynchronous User-Defined](asynchronous-user-defined-functions.md).</span><span class="sxs-lookup"><span data-stu-id="96a73-112">For more information about asynchronous UDFs, see [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span></span>
    
- <span data-ttu-id="96a73-113">**Conectores de clúster**</span><span class="sxs-lookup"><span data-stu-id="96a73-113">**Cluster Connectors**</span></span>
    
    <span data-ttu-id="96a73-114">Conectores de clúster de habilitar las UDF se ejecuten en clústeres de cálculo de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="96a73-114">Cluster connectors enable UDFs to run on high-performance compute clusters.</span></span> <span data-ttu-id="96a73-115">Para obtener más información sobre la creación de conectores de clúster, vea [Desarrollo de conectores de clúster de Excel](developing-excel-cluster-connectors.md).</span><span class="sxs-lookup"><span data-stu-id="96a73-115">For more information about creating cluster connectors, see [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="96a73-116">Los complementos XLL que va a ejecutar en clústeres de cálculo deben llamar a funciones de seguridad de clúster sólo.</span><span class="sxs-lookup"><span data-stu-id="96a73-116">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions.</span></span> <span data-ttu-id="96a73-117">Para obtener más información acerca de las funciones pueden usar, vea la [Referencia de funciones de API de SDK de XLL de Excel](excel-xll-sdk-api-function-reference.md) y [Funciones seguras de clúster](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="96a73-117">For more information about the functions you can use, see [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span></span> 
  
- <span data-ttu-id="96a73-118">**compatibilidad con 64 bits**</span><span class="sxs-lookup"><span data-stu-id="96a73-118">**64-bit Support**</span></span>
    
    <span data-ttu-id="96a73-119">Ahora puede compilar y vincular los XLL de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="96a73-119">You can now compile and link both 32-bit and 64-bit XLLs.</span></span> <span data-ttu-id="96a73-120">Para obtener más información, vea [Creación de XLL](creating-xlls.md).</span><span class="sxs-lookup"><span data-stu-id="96a73-120">For more information, see [Creating XLLs](creating-xlls.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96a73-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="96a73-121">See also</span></span>



[<span data-ttu-id="96a73-122">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="96a73-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="96a73-123">Programar con la API de C en Excel</span><span class="sxs-lookup"><span data-stu-id="96a73-123">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
[<span data-ttu-id="96a73-124">Subprocesamiento m�ltiple y la contenci�n de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="96a73-124">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)


[<span data-ttu-id="96a73-125">Introducci�n al SDK de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="96a73-125">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

