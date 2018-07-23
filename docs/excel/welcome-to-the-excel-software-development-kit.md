---
title: Kit de desarrollo de software Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- excel 2007 xll software development kit,add-ins [Excel 2007]
localization_priority: Normal
ms.assetid: abfc9d76-6f22-49b9-ba45-eb7a54b082e0
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4de88a12b5fb945c6243e52b77babe88b2d02417
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815708"
---
# <a name="welcome-to-the-excel-software-development-kit"></a><span data-ttu-id="eb747-104">Kit de desarrollo de software Excel</span><span class="sxs-lookup"><span data-stu-id="eb747-104">Welcome to the Excel Software Development Kit</span></span>

 <span data-ttu-id="eb747-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="eb747-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="eb747-p101">Bienvenido a la documentación del Kit de desarrollo de software de XLL (SDK) de Excel 2013. Esta referencia contiene información general conceptual, tareas de programación y ejemplos para ayudarle a desarrollar los XLL de Microsoft Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="eb747-p101">Welcome to the Excel 2013 XLL Software Development Kit (SDK) documentation. This reference contains conceptual overviews, programming tasks, and samples to help you develop Microsoft Excel 2013 XLLs.</span></span>
  
<span data-ttu-id="eb747-108">Revisado: Noviembre de 2012</span><span class="sxs-lookup"><span data-stu-id="eb747-108">Revised: November 2012</span></span>
  
<span data-ttu-id="eb747-109">Descargue el [SDK de XLL de Excel 2013](http://go.microsoft.com/fwlink/?LinkID=251082&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="eb747-109">Download the [Excel 2013 XLL SDK](http://go.microsoft.com/fwlink/?LinkID=251082&amp;clcid=0x409).</span></span>
  
<span data-ttu-id="eb747-110">El SDK de XLL de Excel 2013 incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="eb747-110">The Excel 2013 XLL SDK includes the following:</span></span>
  
- <span data-ttu-id="eb747-111">**Interfaz de programación de aplicaciones C (API)**: incluye archivos de origen y de encabezado que permiten que los DLL accedan a la funcionalidad de Excel 2013 y una descripción de la interfaz que debe exponer un DLL para trabajar con el Administrador de complementos de Excel.</span><span class="sxs-lookup"><span data-stu-id="eb747-111">**C application programming interface (API)**—Includes header and source files that enable DLLs to access Excel 2013 functionality, and a description of the interface that a DLL should expose to work with the Excel Add-in Manager.</span></span>
    
- <span data-ttu-id="eb747-p102">**Proyectos de Microsoft Visual Studio**: incluye el código fuente de C/C++ y muestra cómo usar la API de C. Estos proyectos de ejemplo proporcionan ejemplo y sirven como punto de inicio para el desarrollo de complementos.</span><span class="sxs-lookup"><span data-stu-id="eb747-p102">**Microsoft Visual Studio projects**—Includes C/C++ source code and shows how to use the C API. These sample projects provide examples and they serve as a starting point for your own add-in development.</span></span>
    
<span data-ttu-id="eb747-114">La documentación del SDK contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="eb747-114">The SDK documentation contains the following sections:</span></span>
  
- [<span data-ttu-id="eb747-115">Introducción al SDK de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="eb747-115">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)
    
- [<span data-ttu-id="eb747-116">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="eb747-116">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
    
- [<span data-ttu-id="eb747-117">Desarrollo de conectores de cl�ster de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="eb747-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
    
- [<span data-ttu-id="eb747-118">Referencia de funciones de API de SDK de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="eb747-118">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)
    
## <a name="functionality-not-covered"></a><span data-ttu-id="eb747-119">Funcionalidades no cubiertas</span><span class="sxs-lookup"><span data-stu-id="eb747-119">Functionality Not Covered</span></span>

<span data-ttu-id="eb747-120">No se tratan los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="eb747-120">The following subjects are not covered:</span></span>
  
- <span data-ttu-id="eb747-121">Desarrollo de funciones definidas por el usuario y comandos en hojas de macros de Excel (XLM).</span><span class="sxs-lookup"><span data-stu-id="eb747-121">Developing user-defined functions and commands in Excel macro (XLM) sheets.</span></span>
    
- <span data-ttu-id="eb747-122">Creación de funciones definidas por el usuario en DLL que controlan el flujo de ejecución de una macro XLM.</span><span class="sxs-lookup"><span data-stu-id="eb747-122">Creating user-defined functions in DLLs that control the flow of execution of an XLM macro.</span></span>
    
    <span data-ttu-id="eb747-123">Estas funciones funcionan devolviendo un tipo de datos de control de flujo especial, que tampoco se describe en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="eb747-123">Such functions work by returning a special flow control data type, which is also not described in this documentation.</span></span>
    
## <a name="related-links"></a><span data-ttu-id="eb747-124">Vínculos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb747-124">Related Links</span></span>

[<span data-ttu-id="eb747-125">Centro de desarrollo de Excel</span><span class="sxs-lookup"><span data-stu-id="eb747-125">Excel Developer Center</span></span>](http://msdn.microsoft.com/es-ES/office/aa905411.aspx)
  
[<span data-ttu-id="eb747-126">Centro para desarrolladores de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="eb747-126">Microsoft Office Developer Center</span></span>](http://msdn.microsoft.com/es-ES/office/default.aspx)
  
[<span data-ttu-id="eb747-127">SDK de Excel 2010: Kit de desarrollo de software de XLL de Excel 2010</span><span class="sxs-lookup"><span data-stu-id="eb747-127">Excel 2010 SDK: Excel 2010 XLL Software Development Kit</span></span>](http://go.microsoft.com/fwlink/?LinkID=186435&amp;clcid=0x409)
  

