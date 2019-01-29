---
title: Desarrollo de XLL de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- complementos - [excel 2007], desarrollo de XLL - [Excel 2007], XLL - [Excel 2007], desarrollo
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d05041f2629694c4a96240ea83b6e84b17f9be38
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701098"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="428e9-104">Desarrollo de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="428e9-104">Developing Excel XLLs</span></span>

<span data-ttu-id="428e9-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="428e9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="428e9-106">El motivo principal para escribir XLL de Microsoft Excel y usar la API de C es crear funciones de hoja de cálculo de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="428e9-106">The primary reason for writing XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="428e9-107">Las aplicaciones de funciones de alto rendimiento y, comenzando en Excel 2007, la capacidad para escribir interfaces multiproceso en recursos de servidor potentes, hacen que sea una parte muy importante de la extensibilidad de Excel.</span><span class="sxs-lookup"><span data-stu-id="428e9-107">Nevertheless, the applications of high-performance functions—and, in Excel 2013, the ability to write multithreaded interfaces to powerful server resources—make this a very important part of Excel extensibility.</span></span> <span data-ttu-id="428e9-108">El rendimiento de XLL se mejoró aún más en Excel 2007 mediante la incorporación de nuevos tipos de datos y, lo que es más importante, la compatibilidad con multiproceso.</span><span class="sxs-lookup"><span data-stu-id="428e9-108">The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="428e9-109">La API de C no tiene ninguna de las características de desarrollo rápido de nivel superior de Microsoft Visual Basic para Aplicaciones (VBA), COM o Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="428e9-109">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework.</span></span> <span data-ttu-id="428e9-110">La administración de memoria es de bajo nivel y, por lo tanto, da mayor responsabilidad al desarrollador.</span><span class="sxs-lookup"><span data-stu-id="428e9-110">Memory management is low level and, therefore, puts greater responsibility on the developer.</span></span> <span data-ttu-id="428e9-111">Muchas características de Excel expuestas a través de COM, para que estén disponibles a través de VBA y .NET Framework, no están expuestas en la API de C.</span><span class="sxs-lookup"><span data-stu-id="428e9-111">Many Excel features that are exposed via COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="428e9-112">Conceptos de programación de Excel</span><span class="sxs-lookup"><span data-stu-id="428e9-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="428e9-113">Trabajar con DLL</span><span class="sxs-lookup"><span data-stu-id="428e9-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="428e9-114">Obtener acceso a código XLL en Excel</span><span class="sxs-lookup"><span data-stu-id="428e9-114">Accessing XLL code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- [<span data-ttu-id="428e9-115">Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo Reemplazar</span><span class="sxs-lookup"><span data-stu-id="428e9-115">Call XLL functions from the Function Wizard or Replace dialog boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [<span data-ttu-id="428e9-116">Llamar a Excel desde el archivo DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="428e9-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="428e9-117">Crear XLL</span><span class="sxs-lookup"><span data-stu-id="428e9-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="428e9-118">Evaluar los nombres y otras expresiones de fórmulas de la hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="428e9-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="428e9-119">Multiproceso y administración de la memoria</span><span class="sxs-lookup"><span data-stu-id="428e9-119">Multithreading and memory management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="428e9-120">Funciones asincrónicas definidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="428e9-120">Asynchronous user-defined functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="428e9-121">Funciones seguras para clústeres</span><span class="sxs-lookup"><span data-stu-id="428e9-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="428e9-122">Permitir interrupciones de usuarios en operaciones largas</span><span class="sxs-lookup"><span data-stu-id="428e9-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="428e9-123">Mostrar cuadros de diálogo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="428e9-123">Displaying dialog boxes from within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="428e9-124">Obtener acceso a la instancia de Excel y los controladores de la ventana principal</span><span class="sxs-lookup"><span data-stu-id="428e9-124">Access Excel instance and main window handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="428e9-125">Compatibilidad con versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="428e9-125">Backward compatibility</span></span>](backward-compatibility.md)
  

