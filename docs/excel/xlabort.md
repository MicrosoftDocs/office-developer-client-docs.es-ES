---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- función xlAbort [excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e90cbe496404b4cc602dee1ad21c91c8f5f91bfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815719"
---
# <a name="xlabort"></a><span data-ttu-id="a675a-104">xlAbort</span><span class="sxs-lookup"><span data-stu-id="a675a-104">xlAbort</span></span>

 <span data-ttu-id="a675a-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a675a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a675a-106">Da como resultado el procesador para otras tareas en el sistema y comprueba si el usuario ha presionado la **tecla ESC** para cancelar una macro.</span><span class="sxs-lookup"><span data-stu-id="a675a-106">Yields the processor to other tasks in the system and checks whether the user has pressed **ESC** to cancel a macro.</span></span> <span data-ttu-id="a675a-107">Si el usuario ha presionado la **tecla ESC** durante una actualización de libros, también se detectan desde dentro de una función de hoja de cálculo mediante una llamada a esta función.</span><span class="sxs-lookup"><span data-stu-id="a675a-107">If the user has pressed **ESC** during a workbook recalculation, it can also be detected from within a worksheet function by calling this function.</span></span> 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a><span data-ttu-id="a675a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a675a-108">Parameters</span></span>

 <span data-ttu-id="a675a-109">_pxRetain_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="a675a-109">_pxRetain_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="a675a-110">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="a675a-110">(Optional).</span></span> <span data-ttu-id="a675a-111">Si es **FALSE**, esta función comprueba la condición de salto y borra cualquier punto de interrupción pendiente.</span><span class="sxs-lookup"><span data-stu-id="a675a-111">If **FALSE**, this function checks for the break condition and clears any pending break.</span></span> <span data-ttu-id="a675a-112">Esto permite al usuario continuar a pesar de la condición de interrupción.</span><span class="sxs-lookup"><span data-stu-id="a675a-112">This enables the user to continue despite the break condition.</span></span> <span data-ttu-id="a675a-113">Si este argumento se omite o es **TRUE**, la función comprueba una anulación de usuario sin borrarlo.</span><span class="sxs-lookup"><span data-stu-id="a675a-113">If this argument is omitted or is **TRUE**, the function checks for a user abort without clearing it.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a675a-114">Propiedad valor y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a675a-114">Property value/Return value</span></span>

<span data-ttu-id="a675a-115">Devuelve **TRUE** (**xltypeBool**) si el usuario ha presionado la **tecla ESC**.</span><span class="sxs-lookup"><span data-stu-id="a675a-115">Returns **TRUE** (**xltypeBool**) if the user has pressed **ESC**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a675a-116">Notas</span><span class="sxs-lookup"><span data-stu-id="a675a-116">Remarks</span></span>

### 

#### <a name="frequent-calls-may-be-needed"></a><span data-ttu-id="a675a-117">Las llamadas frecuentes que puedan ser necesarios</span><span class="sxs-lookup"><span data-stu-id="a675a-117">Frequent Calls May Be Needed</span></span>

<span data-ttu-id="a675a-118">Funciones y comandos que podrían tardar mucho tiempo deben llamar a esta función con frecuencia para producir el procesador para otras tareas en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a675a-118">Functions and commands that could take a long time should call this function frequently to yield the processor to other tasks in the system.</span></span>
  
#### <a name="avoid-sensitive-language"></a><span data-ttu-id="a675a-119">Evitar idioma confidencial</span><span class="sxs-lookup"><span data-stu-id="a675a-119">Avoid Sensitive Language</span></span>

<span data-ttu-id="a675a-120">Evitar el uso de los términos "Anular" en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a675a-120">Avoid using the term "Abort" in your user interface.</span></span> <span data-ttu-id="a675a-121">Considere el uso de "Cancelar", "Detener", "Romper" o "Stop" en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a675a-121">Consider using "Cancel," "Halt," "Break," or "Stop" instead.</span></span>
  
## <a name="example"></a><span data-ttu-id="a675a-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a675a-122">Example</span></span>

<span data-ttu-id="a675a-123">El siguiente código repetidamente mueve la celda activa en una hoja de hasta que haya transcurrido un minuto o hasta que el usuario presiona la **tecla ESC**.</span><span class="sxs-lookup"><span data-stu-id="a675a-123">The following code repeatedly moves the active cell on a sheet until one minute has elapsed or until the user presses **ESC**.</span></span> <span data-ttu-id="a675a-124">Llama a la función **xlAbort** ocasionalmente.</span><span class="sxs-lookup"><span data-stu-id="a675a-124">It calls the function **xlAbort** occasionally.</span></span> <span data-ttu-id="a675a-125">Esto da como resultado el procesador, cooperación multitarea de aceleración.</span><span class="sxs-lookup"><span data-stu-id="a675a-125">This yields the processor, easing cooperative multitasking.</span></span> 
  
 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
int WINAPI fDance(void)
{
   DWORD dtickStart;
   XLOPER12 xAbort, xConfirm;
   int boolSheet;
   int col=0;
   XCHAR rgch[32];
//
// Check what kind of sheet is active. If it is a worksheet or macro
// sheet, this function will move the selection in a loop to show
// activity. In any case, it will update the status bar with a countdown.
//
// Call xlSheetId; if that fails the current sheet is not a macro sheet or
// worksheet. Next, get the time at which to start. Then start a while
// loop that will run for one minute. During the while loop, check if the
// user has pressed ESC. If true, confirm the abort. If the abort is
// confirmed, clear the message bar and return; if the abort is not
// confirmed, clear the abort state and continue. After checking for an
// abort, move the active cell if on a worksheet or macro. Then
// update the status bar with the time remaining.
//
// This block uses TempActiveCell12(), which creates a temporary XLOPER12.
// The XLOPER12 contains a reference to a single cell on the active sheet.
// This function is part of the framework library.
//
   boolSheet = (Excel12f(xlSheetId, 0, 0) == xlretSuccess);
   dtickStart = GetTickCount();
   while (GetTickCount() < dtickStart + 60000L)
   {
      Excel12f(xlAbort, &xAbort, 0);
      if (xAbort.val.xbool)
      {
         Excel12f(xlcAlert, &xConfirm, 2,
           TempStr12(L"Are you sure you want to cancel this operation?"),
              TempNum12(1));
         if (xConfirm.val.xbool)
         {
            Excel12f(xlcMessage, 0, 1, TempBool12(0));
            return 1;
         }
         else
         {
            Excel12f(xlAbort, 0, 1, TempBool12(0));
         }
      }
      if (boolSheet)
      {
         Excel12f(xlcSelect, 0, 1,
            TempActiveCell12(0,(BYTE)col));
         col = (col + 1) & 3;
      }
      wsprintfW(rgch,L"0:%lu",
         (60000 + dtickStart - GetTickCount()) / 1000L);
      Excel12f(xlcMessage, 0, 2, TempBool12(1), TempStr12(rgch));
   }
   Excel12f(xlcMessage, 0, 1, TempBool12(0));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a675a-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="a675a-126">See also</span></span>



[<span data-ttu-id="a675a-127">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="a675a-127">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

