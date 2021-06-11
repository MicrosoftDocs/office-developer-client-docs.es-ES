---
title: Controlar eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c989bc39c22f4e566c18feb4fdeaa8582c5525f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438270"
---
# <a name="handling-events"></a><span data-ttu-id="e8fef-103">Controlar eventos</span><span class="sxs-lookup"><span data-stu-id="e8fef-103">Handling Events</span></span>

 <span data-ttu-id="e8fef-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8fef-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e8fef-105">A partir Excel 2010, los XLL pueden recibir eventos diseñados para administrar el ciclo de vida de la función asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e8fef-105">Starting in Excel 2010, XLLs can receive events designed to manage the asynchronous function life cycle.</span></span> <span data-ttu-id="e8fef-106">Los eventos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8fef-106">The events are as follows:</span></span>
  
- <span data-ttu-id="e8fef-107">**CalculationEnded:** se genera cuando Excel termina de calcular.</span><span class="sxs-lookup"><span data-stu-id="e8fef-107">**CalculationEnded**: Raised when Excel is finished calculating.</span></span> <span data-ttu-id="e8fef-108">Después de este evento, puede liberar los recursos asignados durante el cálculo.</span><span class="sxs-lookup"><span data-stu-id="e8fef-108">After this event, you can free resources allocated during the calculation.</span></span>
    
- <span data-ttu-id="e8fef-109">**CalculationCanceled:** se genera cuando el usuario interrumpe el cálculo.</span><span class="sxs-lookup"><span data-stu-id="e8fef-109">**CalculationCanceled**: Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="e8fef-110">El XLL detiene cualquier actividad asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e8fef-110">The XLL stops any asynchronous activities.</span></span> <span data-ttu-id="e8fef-111">Inmediatamente después de este evento, se genera el **evento CalculationEnded.**</span><span class="sxs-lookup"><span data-stu-id="e8fef-111">Immediately following this event, the **CalculationEnded** event is raised.</span></span> 
    
<span data-ttu-id="e8fef-112">Para controlar estos eventos, XLL usa la función de API de C [xlEventRegister](xleventregister.md).</span><span class="sxs-lookup"><span data-stu-id="e8fef-112">To handle these events, the XLL uses the C API function [xlEventRegister](xleventregister.md).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e8fef-113">**CalculationEnded** y **CalculationCanceled** no se genera durante el recálculo mediante programación.</span><span class="sxs-lookup"><span data-stu-id="e8fef-113">**CalculationEnded** and **CalculationCanceled** are not raised during programmatic recalculation.</span></span> 
  

