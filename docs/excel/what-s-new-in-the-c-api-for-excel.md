---
title: Novedades de la API de C para Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api de c [excel 2007], novedades
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439691"
---
# <a name="whats-new-in-the-c-api-for-excel"></a><span data-ttu-id="6e66f-104">Novedades de la API de C para Excel</span><span class="sxs-lookup"><span data-stu-id="6e66f-104">What's New in the C API for Excel</span></span>

 <span data-ttu-id="6e66f-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6e66f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6e66f-106">Junto con Microsoft Excel 2013, el Kit de desarrollo de software (SDK) XLL de Microsoft Excel 2013 incluye compatibilidad con las siguientes características.</span><span class="sxs-lookup"><span data-stu-id="6e66f-106">In conjunction with Microsoft Excel 2013, the Microsoft Excel 2013 XLL Software Development Kit (SDK) includes support for the following features.</span></span>
  
- <span data-ttu-id="6e66f-107">**Nuevas funciones**</span><span class="sxs-lookup"><span data-stu-id="6e66f-107">**New Functions**</span></span>
    
    <span data-ttu-id="6e66f-108">El SDK de XLL de Microsoft Excel 2013 admite la llamada a todas las nuevas funciones de hoja de cálculo de Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="6e66f-108">The Microsoft Excel 2013 XLL SDK supports calling back to all of the new worksheet functions in Excel 2013.</span></span> <span data-ttu-id="6e66f-109">Para obtener más información acerca de cómo llamar a funciones de Excel 2013, vea Llamar a Excel desde [el DLL o XLL](calling-into-excel-from-the-dll-or-xll.md).</span><span class="sxs-lookup"><span data-stu-id="6e66f-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span></span>
    
- <span data-ttu-id="6e66f-110">**Funciones asincrónicas definidas por el usuario**</span><span class="sxs-lookup"><span data-stu-id="6e66f-110">**Asynchronous User-defined Functions**</span></span>
    
    <span data-ttu-id="6e66f-111">Excel 2013 admite llamadas a funciones definidas por el usuario (UDF) de forma asincrónica, lo que puede mejorar el rendimiento al permitir que se ejecuten varios cálculos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="6e66f-111">Excel 2013 supports calling user-defined functions (UDF) asynchronously, which can improve performance by enabling several calculations to run at the same time.</span></span> <span data-ttu-id="6e66f-112">Para obtener más información acerca de las UDF asincrónicas, vea Funciones de User-Defined [asincrónicas.](asynchronous-user-defined-functions.md)</span><span class="sxs-lookup"><span data-stu-id="6e66f-112">For more information about asynchronous UDFs, see [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span></span>
    
- <span data-ttu-id="6e66f-113">**Conectores de clúster**</span><span class="sxs-lookup"><span data-stu-id="6e66f-113">**Cluster Connectors**</span></span>
    
    <span data-ttu-id="6e66f-114">Los conectores de clúster permiten que las UDF se ejecuten en clústeres de cálculo de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="6e66f-114">Cluster connectors enable UDFs to run on high-performance compute clusters.</span></span> <span data-ttu-id="6e66f-115">Para obtener más información acerca de la creación de conectores de clúster, vea [Desarrollar conectores de clúster de Excel.](developing-excel-cluster-connectors.md)</span><span class="sxs-lookup"><span data-stu-id="6e66f-115">For more information about creating cluster connectors, see [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6e66f-116">Los complementos XLL que desea ejecutar en clústeres de cálculo solo deben llamar a funciones seguras para clústeres.</span><span class="sxs-lookup"><span data-stu-id="6e66f-116">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions.</span></span> <span data-ttu-id="6e66f-117">Para obtener más información acerca de las funciones que puede usar, vea Referencia de funciones de API de SDK de [XLL](excel-xll-sdk-api-function-reference.md) de Excel y [Funciones seguras de clúster.](cluster-safe-functions.md)</span><span class="sxs-lookup"><span data-stu-id="6e66f-117">For more information about the functions you can use, see [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span></span> 
  
- <span data-ttu-id="6e66f-118">**Compatibilidad de 64 bits**</span><span class="sxs-lookup"><span data-stu-id="6e66f-118">**64-bit Support**</span></span>
    
    <span data-ttu-id="6e66f-119">Ahora puede compilar y vincular XLL de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6e66f-119">You can now compile and link both 32-bit and 64-bit XLLs.</span></span> <span data-ttu-id="6e66f-120">Para obtener más información, vea [Crear XLL.](creating-xlls.md)</span><span class="sxs-lookup"><span data-stu-id="6e66f-120">For more information, see [Creating XLLs](creating-xlls.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e66f-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6e66f-121">See also</span></span>



[<span data-ttu-id="6e66f-122">Desarrollar archivos XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="6e66f-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="6e66f-123">Programar con la API de C en Excel</span><span class="sxs-lookup"><span data-stu-id="6e66f-123">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
[<span data-ttu-id="6e66f-124">Multiproceso y conflictos de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="6e66f-124">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)


[<span data-ttu-id="6e66f-125">Introducción al SDK de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="6e66f-125">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

