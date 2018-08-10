---
title: Desarrollo de XLL de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- complementos - [excel 2007], el desarrollo de XLL - [Excel 2007], XLL - [Excel 2007], desarrollo
localization_priority: Normal
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cb2483b9cd1b11bcfeee81bba02b6d593e8818fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815534"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="535b6-104">Desarrollo de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="535b6-104">Developing Excel XLLs</span></span>

<span data-ttu-id="535b6-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="535b6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="535b6-106">La razón principal para escribir los XLL de Microsoft Excel y uso de la API de C es crear funciones de hoja de cálculo de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="535b6-106">The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="535b6-107">Las aplicaciones de funciones de alto rendimiento: y, a partir de Excel 2007, la capacidad de escribir interfaces multiproceso en recursos de servidor eficaces: realizar una parte muy importante de la extensibilidad de Excel.</span><span class="sxs-lookup"><span data-stu-id="535b6-107">The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility.</span></span> <span data-ttu-id="535b6-108">El rendimiento de los XLL estaba más mejorada en Excel 2007 mediante la adición de nuevos tipos de datos y, más importante, compatibilidad con subprocesamiento múltiple.</span><span class="sxs-lookup"><span data-stu-id="535b6-108">The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="535b6-109">La API C no tiene ninguna de las características de desarrollo rápido de nivel superior de Microsoft Visual Basic para aplicaciones (VBA), COM o Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="535b6-109">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework.</span></span> <span data-ttu-id="535b6-110">Administración de memoria es nivel bajo y por lo tanto, delega mayor responsabilidad en el programador.</span><span class="sxs-lookup"><span data-stu-id="535b6-110">Memory management is low level, and therefore puts greater responsibility on the developer.</span></span> <span data-ttu-id="535b6-111">Muchas características de Excel que se exponen a través de COM, habilitarlos a través de VBA y .NET Framework, no se exponen a la API de C.</span><span class="sxs-lookup"><span data-stu-id="535b6-111">Many Excel features that are exposed through COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="535b6-112">Conceptos de programación de Excel</span><span class="sxs-lookup"><span data-stu-id="535b6-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="535b6-113">Trabajar con DLL</span><span class="sxs-lookup"><span data-stu-id="535b6-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="535b6-114">Obtener acceso a código XLL en Excel</span><span class="sxs-lookup"><span data-stu-id="535b6-114">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- [<span data-ttu-id="535b6-115">Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo Reemplazar</span><span class="sxs-lookup"><span data-stu-id="535b6-115">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [<span data-ttu-id="535b6-116">Llamar a Excel desde el archivo DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="535b6-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="535b6-117">Crear XLL</span><span class="sxs-lookup"><span data-stu-id="535b6-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="535b6-118">Evaluar los nombres y otras expresiones de fórmulas de la hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="535b6-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="535b6-119">Multiproceso y administración de la memoria</span><span class="sxs-lookup"><span data-stu-id="535b6-119">Multithreading and Memory Management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="535b6-120">Funciones asincrónicas definidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="535b6-120">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="535b6-121">Funciones de seguridad de grupo</span><span class="sxs-lookup"><span data-stu-id="535b6-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="535b6-122">Permitir interrupciones de usuarios en operaciones largas</span><span class="sxs-lookup"><span data-stu-id="535b6-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="535b6-123">Mostrar cuadros de diálogo de un DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="535b6-123">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="535b6-124">Obtener acceso a la instancia de Excel y los controladores de la ventana principal</span><span class="sxs-lookup"><span data-stu-id="535b6-124">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="535b6-125">Compatibilidad con versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="535b6-125">Backward Compatibility</span></span>](backward-compatibility.md)
  
