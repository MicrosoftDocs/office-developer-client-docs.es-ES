---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 00c222efce6925c3f691eb2b799adf687c22082c
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160282"
---
# <a name="xleventregister"></a><span data-ttu-id="8a88f-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="8a88f-103">xlEventRegister</span></span>

 <span data-ttu-id="8a88f-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8a88f-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8a88f-105">Se usa para registrar un controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="8a88f-105">Used to register an event handler.</span></span> <span data-ttu-id="8a88f-106">Se introdujo en Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="8a88f-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="8a88f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a88f-107">Parameters</span></span>

 <span data-ttu-id="8a88f-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="8a88f-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="8a88f-109">Nombre de la función del controlador de eventos tal como aparece en el código DLL.</span><span class="sxs-lookup"><span data-stu-id="8a88f-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="8a88f-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="8a88f-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="8a88f-111">Evento que controla la función designada en el _parámetro pxProcedure._</span><span class="sxs-lookup"><span data-stu-id="8a88f-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="8a88f-112">A partir de Excel 2010, Excel admite los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="8a88f-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="8a88f-113">**Evento**</span><span class="sxs-lookup"><span data-stu-id="8a88f-113">**Event**</span></span>|<span data-ttu-id="8a88f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8a88f-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a88f-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="8a88f-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="8a88f-116">Se genera cuando Excel completa un cálculo.</span><span class="sxs-lookup"><span data-stu-id="8a88f-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="8a88f-117">Puede liberar los recursos asignados durante el cálculo después de este evento.</span><span class="sxs-lookup"><span data-stu-id="8a88f-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="8a88f-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="8a88f-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="8a88f-119">Se genera cuando el usuario interrumpe el cálculo.</span><span class="sxs-lookup"><span data-stu-id="8a88f-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="8a88f-120">El XLL debe detener cualquier actividad asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8a88f-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="8a88f-121">El evento CalculationEnded se genera inmediatamente después de este evento.</span><span class="sxs-lookup"><span data-stu-id="8a88f-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="8a88f-122">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a88f-122">Property value/Return value</span></span>

<span data-ttu-id="8a88f-123">Si se realiza correctamente, pxRes (**xltypeInt**) tiene un valor > 0.</span><span class="sxs-lookup"><span data-stu-id="8a88f-123">If successful, pxRes (**xltypeInt**) has a value > 0.</span></span> <span data-ttu-id="8a88f-124">Si no se realiza correctamente, pxRes ==0.</span><span class="sxs-lookup"><span data-stu-id="8a88f-124">If unsuccessful, pxRes ==0.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8a88f-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8a88f-125">See also</span></span>



[<span data-ttu-id="8a88f-126">Funciones asincrónicas definidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="8a88f-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

