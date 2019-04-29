---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 869122954ffe3928dfea72b8fc9fb432b9979e42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438767"
---
# <a name="xleventregister"></a><span data-ttu-id="238c5-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="238c5-103">xlEventRegister</span></span>

 <span data-ttu-id="238c5-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="238c5-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="238c5-105">Se usa para registrar un controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="238c5-105">Used to register an event handler.</span></span> <span data-ttu-id="238c5-106">Se ha incluido en Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="238c5-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="238c5-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="238c5-107">Parameters</span></span>

 <span data-ttu-id="238c5-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="238c5-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="238c5-109">El nombre de la función del controlador de eventos tal como aparece en el código de DLL.</span><span class="sxs-lookup"><span data-stu-id="238c5-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="238c5-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="238c5-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="238c5-111">El evento controlado por la función designada en el parámetro _pxProcedure_ .</span><span class="sxs-lookup"><span data-stu-id="238c5-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="238c5-112">A partir de Excel 2010, Excel admite los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="238c5-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="238c5-113">**Event**</span><span class="sxs-lookup"><span data-stu-id="238c5-113">**Event**</span></span>|<span data-ttu-id="238c5-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="238c5-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="238c5-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="238c5-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="238c5-116">Se produce cuando Excel completa un cálculo.</span><span class="sxs-lookup"><span data-stu-id="238c5-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="238c5-117">Puede liberar los recursos asignados durante el cálculo después de este evento.</span><span class="sxs-lookup"><span data-stu-id="238c5-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="238c5-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="238c5-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="238c5-119">Se produce cuando el usuario interrumpe el cálculo.</span><span class="sxs-lookup"><span data-stu-id="238c5-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="238c5-120">El XLL debe detener todas las actividades asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="238c5-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="238c5-121">El evento CalculationEnded se genera inmediatamente después de este evento.</span><span class="sxs-lookup"><span data-stu-id="238c5-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="238c5-122">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="238c5-122">Property value/Return value</span></span>

<span data-ttu-id="238c5-123">Si se ejecuta correctamente, devuelve **true** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="238c5-123">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="238c5-124">Si no se realiza correctamente, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="238c5-124">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="238c5-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="238c5-125">See also</span></span>



[<span data-ttu-id="238c5-126">Funciones asincrónicas definidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="238c5-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

