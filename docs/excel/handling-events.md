---
title: Controlar eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: c5508df8466932b6fb5c7e04164aa00a5ea31a8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815631"
---
# <a name="handling-events"></a><span data-ttu-id="6e300-103">Controlar eventos</span><span class="sxs-lookup"><span data-stu-id="6e300-103">Handling Events</span></span>

 <span data-ttu-id="6e300-104">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6e300-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6e300-105">Iniciar en Excel 2010, XLL pueden recibir eventos diseñados para administrar el ciclo de vida de la función asincrónica.</span><span class="sxs-lookup"><span data-stu-id="6e300-105">Starting in Excel 2010, XLLs can receive events designed to manage the asynchronous function life cycle.</span></span> <span data-ttu-id="6e300-106">Los eventos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6e300-106">The events are as follows:</span></span>
  
- <span data-ttu-id="6e300-107">**CalculationEnded**: se produce cuando finalice Excel calcular.</span><span class="sxs-lookup"><span data-stu-id="6e300-107">**CalculationEnded**: Raised when Excel is finished calculating.</span></span> <span data-ttu-id="6e300-108">Después de este evento, puede liberar recursos asignados durante el cálculo.</span><span class="sxs-lookup"><span data-stu-id="6e300-108">After this event, you can free resources allocated during the calculation.</span></span>
    
- <span data-ttu-id="6e300-109">**CalculationCanceled**: se produce cuando el usuario los cálculos interrumpe el cálculo.</span><span class="sxs-lookup"><span data-stu-id="6e300-109">**CalculationCanceled**: Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="6e300-110">El XLL detiene cualquier actividades asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="6e300-110">The XLL stops any asynchronous activities.</span></span> <span data-ttu-id="6e300-111">Inmediatamente después de este evento se desencadena el evento **CalculationEnded** .</span><span class="sxs-lookup"><span data-stu-id="6e300-111">Immediately following this event, the **CalculationEnded** event is raised.</span></span> 
    
<span data-ttu-id="6e300-112">Para controlar estos eventos, el XLL usa la función de API C [xlEventRegister](xleventregister.md).</span><span class="sxs-lookup"><span data-stu-id="6e300-112">To handle these events, the XLL uses the C API function [xlEventRegister](xleventregister.md).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6e300-113">**CalculationEnded** y **CalculationCanceled** no se ha generado durante la actualización mediante programación.</span><span class="sxs-lookup"><span data-stu-id="6e300-113">**CalculationEnded** and **CalculationCanceled** are not raised during programmatic recalculation.</span></span> 
  

