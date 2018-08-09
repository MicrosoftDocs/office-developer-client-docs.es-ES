---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815729"
---
# <a name="xleventregister"></a><span data-ttu-id="00845-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="00845-103">xlEventRegister</span></span>

 <span data-ttu-id="00845-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="00845-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="00845-105">Se usa para registrar un controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="00845-105">Used to register an event handler.</span></span> <span data-ttu-id="00845-106">Introdujo en Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="00845-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="00845-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00845-107">Parameters</span></span>

 <span data-ttu-id="00845-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="00845-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="00845-109">El nombre de la función de controlador de eventos tal como se muestra en el código del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="00845-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="00845-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="00845-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="00845-111">El evento controlado por la función designada en el parámetro _pxProcedure_ .</span><span class="sxs-lookup"><span data-stu-id="00845-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="00845-112">A partir de Excel 2010, Excel admite los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="00845-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="00845-113">**Evento**</span><span class="sxs-lookup"><span data-stu-id="00845-113">**Event**</span></span>|<span data-ttu-id="00845-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00845-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00845-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="00845-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="00845-116">Se produce cuando Excel completa un cálculo.</span><span class="sxs-lookup"><span data-stu-id="00845-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="00845-117">Puede liberar cualquier recurso asignado durante el cálculo después de este evento.</span><span class="sxs-lookup"><span data-stu-id="00845-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="00845-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="00845-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="00845-119">Se produce cuando el usuario los cálculos interrumpe el cálculo.</span><span class="sxs-lookup"><span data-stu-id="00845-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="00845-120">El XLL debe detener cualquier actividad asincrónica.</span><span class="sxs-lookup"><span data-stu-id="00845-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="00845-121">El evento CalculationEnded se produce inmediatamente después de este evento.</span><span class="sxs-lookup"><span data-stu-id="00845-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="00845-122">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00845-122">Property value/Return value</span></span>

<span data-ttu-id="00845-123">Si se realiza correctamente, devuelve **TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="00845-123">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="00845-124">Si no lo consigue, devuelve **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="00845-124">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="00845-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="00845-125">See also</span></span>



[<span data-ttu-id="00845-126">Funciones asincrónicas definidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="00845-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

